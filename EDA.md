# EDA (Exploratory Data Analysis)

## Objetivo

El EDA (Exploratory Data Analysis o Análisis Exploratorio de Datos) es el proceso de inspeccionar, limpiar, comprender y visualizar los datos antes de realizar análisis avanzados o construir modelos.

Responde preguntas como:

- ¿Qué información contiene el dataset?
- ¿Existen errores en los datos?
- ¿Hay valores nulos?
- ¿Existen outliers?
- ¿Qué variables son importantes?
- ¿Cómo se distribuyen los datos?
- ¿Existen relaciones entre variables?

---

# ¿Por Qué es Importante?

En proyectos reales:

```text
80% del tiempo
=
Entender y preparar datos

20% del tiempo
=
Modelar y analizar
```

Muchos errores de análisis provienen de:

- Datos incompletos.
- Datos duplicados.
- Valores extremos.
- Tipos de dato incorrectos.
- Interpretaciones erróneas.

---

# Mentalidad del Analista

Antes de responder cualquier pregunta:

❌ No construir modelos.

❌ No crear dashboards.

❌ No sacar conclusiones.

Primero:

✅ Conocer los datos.

✅ Entender los patrones.

✅ Detectar problemas.

---

# Flujo General del EDA

```text
Obtener Datos
      ↓
Entender Estructura
      ↓
Evaluar Calidad
      ↓
Analizar Distribuciones
      ↓
Detectar Outliers
      ↓
Buscar Relaciones
      ↓
Generar Hipótesis
      ↓
Análisis Avanzado
```

---

# Paso 1: Conocer el Dataset

## Pregunta

```text
¿Qué tengo?
```

---

## Primeras Filas

```python
df.head()
```

---

Ejemplo

```text
| Cliente | Edad | Salario |
|----------|--------|---------|
| Ana      | 25     | 5000    |
| Luis     | 30     | 6500    |
```

---

Permite:

- Ver columnas.
- Validar estructura.
- Entender contexto.

---

# Últimas Filas

```python
df.tail()
```

---

Útil para:

- Detectar registros extraños.
- Revisar carga completa.

---

# Dimensiones del Dataset

## Cantidad de Filas y Columnas

```python
df.shape
```

---

Ejemplo

```text
(5000, 12)
```

Interpretación:

```text
5000 registros
12 variables
```

---

# Paso 2: Entender las Variables

## Ver Nombres

```python
df.columns
```

---

Resultado

```text
Edad
Salario
Departamento
Antiguedad
```

---

## Ver Tipos

```python
df.dtypes
```

---

Ejemplo

```text
Edad           int64
Salario        float64
FechaIngreso   datetime
Nombre         object
```

---

# Tipos de Variables

## Numéricas

Ejemplos:

```text
Edad
Ventas
Salario
Tiempo
```

---

## Categóricas

Ejemplos:

```text
Departamento
Estado
Ciudad
Sexo
```

---

## Fechas

Ejemplos:

```text
FechaVenta
FechaIngreso
FechaResolucion
```

---

# Información General

```python
df.info()
```

---

Permite visualizar:

- Tipos de dato.
- Valores nulos.
- Cantidad de registros.

---

# Paso 3: Evaluar Calidad de Datos

## Pregunta

```text
¿Los datos son confiables?
```

---

# Valores Nulos

## Detección

```python
df.isnull().sum()
```

---

Resultado

```text
Edad         0
Salario      5
Ciudad      20
```

---

Interpretación

```text
Salario tiene 5 registros vacíos.
```

---

# Duplicados

## Detección

```python
df.duplicated().sum()
```

---

Interpretación

```text
¿Existe información repetida?
```

---

# Valores Inconsistentes

Ejemplos:

```text
Masculino
masculino
MASCULINO
M
```

---

Problema:

```text
Representan lo mismo
pero se registraron diferente.
```

---

# Paso 4: Estadística Descriptiva

## Pregunta

```text
¿Cómo se comportan los datos?
```

---

# Resumen Estadístico

```python
df.describe()
```

---

Resultado típico

```text
count
mean
std
min
25%
50%
75%
max
```

---

# Interpretación

## Mean

```text
Promedio
```

---

## Std

```text
Dispersión
```

---

## 50%

```text
Mediana
```

---

## 25% y 75%

```text
Cuartiles
```

---

# Ejemplo

```text
Salario

Mean = 8000

50% = 7000
```

---

Interpretación

```text
Media y mediana diferentes.

Probable sesgo positivo.
```

---

# Paso 5: Analizar Distribuciones

## Histograma

```python
df["Salario"].hist()
```

---

o

```python
sns.histplot(
    df["Salario"],
    kde=True
)
```

---

Objetivo:

- Detectar forma.
- Detectar asimetría.
- Detectar agrupaciones.

---

# Interpretación

## Distribución Normal

```text
       █
     █████
   █████████
 █████████████
   █████████
     █████
       █
```

---

## Sesgo Positivo

```text
████████
█████
███
█
```

---

Ejemplo:

```text
Salarios.
Ventas.
Patrimonio.
```

---

# Paso 6: Detectar Outliers

## BoxPlot

```python
sns.boxplot(
    x=df["Salario"]
)
```

---

Visualización

```text
              ●

|-----|=====|-----|
```

---

Interpretación

```text
Posible valor atípico.
```

---

# Preguntas

- ¿Es un error?
- ¿Es un caso especial?
- ¿Debe eliminarse?

---

# Paso 7: Entender Variables Categóricas

## Conteo de Categorías

```python
df["Departamento"].value_counts()
```

---

Resultado

```text
Ventas       200
IT           150
Finanzas     100
```

---

# Visualización

```python
sns.countplot(
    x="Departamento",
    data=df
)
```

---

Pregunta:

```text
¿Cuáles categorías dominan?
```

---

# Paso 8: Analizar Relaciones

## Correlación

```python
df.corr()
```

---

Ejemplo

```text
Edad vs Salario

0.70
```

---

Interpretación

```text
Relación positiva fuerte.
```

---

# Heatmap

```python
sns.heatmap(
    df.corr(),
    annot=True
)
```

---

Permite identificar:

- Variables relacionadas.
- Variables redundantes.
- Posibles predictores.

---

# Scatter Plot

```python
sns.scatterplot(
    x="Edad",
    y="Salario",
    data=df
)
```

---

Pregunta:

```text
¿Existe relación visual?
```

---

# Paso 9: Segmentación

Una de las tareas más importantes del EDA.

---

Ejemplo

```python
df.groupby("Departamento")["Salario"].mean()
```

---

Resultado

```text
IT          12000
Ventas       8000
Finanzas    10000
```

---

Interpretación

```text
Los salarios varían por área.
```

---

# Paso 10: Generar Hipótesis

Después del EDA comienzan a surgir preguntas.

---

Ejemplo

Observación:

```text
Clientes con más productos
tienen saldos más altos.
```

---

Hipótesis:

```text
Existe relación entre productos y saldo.
```

---

Posteriormente:

```text
Correlación
Regresión
Machine Learning
```

---

# Ejemplo Completo de EDA

Supongamos un dataset bancario.

Variables:

```text
Edad
Saldo
Productos
Ciudad
Morosidad
```

---

Preguntas típicas

```text
¿Cuál es la edad promedio?

¿Hay clientes duplicados?

¿Existen saldos negativos?

¿Qué ciudades tienen más clientes?

¿Qué relación existe entre saldo y productos?

¿Quiénes son los clientes más riesgosos?
```

---

Todas forman parte del EDA.

---

# EDA en Pandas

## Resumen Rápido

```python
df.head()

df.info()

df.shape

df.describe()

df.isnull().sum()

df.duplicated().sum()

df.corr()
```

---

# EDA en Seaborn

## Histogramas

```python
sns.histplot()
```

---

## BoxPlots

```python
sns.boxplot()
```

---

## Scatter Plots

```python
sns.scatterplot()
```

---

## Heatmaps

```python
sns.heatmap()
```

---

## Countplots

```python
sns.countplot()
```

---

# Checklist de EDA

Cuando recibas un dataset nuevo:

## Estructura

```text
□ Revisar columnas
□ Revisar filas
□ Revisar dimensiones
```

---

## Calidad

```text
□ Buscar nulos
□ Buscar duplicados
□ Buscar inconsistencias
```

---

## Estadística

```text
□ Media
□ Mediana
□ Desviación estándar
□ Cuartiles
```

---

## Distribución

```text
□ Histogramas
□ Boxplots
□ Outliers
```

---

## Relaciones

```text
□ Correlaciones
□ Scatterplots
```

---

## Negocio

```text
□ Identificar patrones
□ Formular hipótesis
□ Detectar oportunidades
```

---

# Relación con Todo lo Estudiado

```text
Población y Muestra
         ↓
Variables
         ↓
Media y Mediana
         ↓
Varianza
         ↓
Cuartiles
         ↓
Histogramas
         ↓
Distribución Normal
         ↓
Correlación
         ↓
EDA
         ↓
Machine Learning
```

---

# Preguntas que Responde

- ¿Qué contienen los datos?
- ¿Son confiables?
- ¿Existen errores?
- ¿Cómo se distribuyen?
- ¿Hay valores atípicos?
- ¿Qué variables son importantes?
- ¿Qué relaciones existen?
- ¿Qué hipótesis puedo investigar?

---

# Cheat Sheet Rápido

| Paso | Pregunta |
|--------|-----------|
| Head | ¿Qué datos tengo? |
| Shape | ¿Cuántos registros hay? |
| Info | ¿Qué tipos existen? |
| Nulls | ¿Hay datos faltantes? |
| Describe | ¿Cómo se comportan? |
| Histograma | ¿Cómo se distribuyen? |
| BoxPlot | ¿Hay outliers? |
| Corr | ¿Qué variables se relacionan? |
| GroupBy | ¿Existen segmentos? |
| Insights | ¿Qué aprendí? |

---

# Regla de Oro para Data Analytics

Nunca construyas un dashboard, una predicción o un modelo de Machine Learning sin haber realizado primero un EDA completo.

El EDA es donde encuentras:

✅ Errores de datos.

✅ Problemas de calidad.

✅ Patrones de negocio.

✅ Relaciones ocultas.

✅ Oportunidades de mejora.

La diferencia entre un programador que usa Pandas y un analista de datos está en la calidad de las preguntas que realiza durante el EDA.
