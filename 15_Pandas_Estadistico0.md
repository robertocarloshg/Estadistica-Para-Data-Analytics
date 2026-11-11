# Pandas Estadístico

## Objetivo

Aprender a utilizar Pandas como una herramienta estadística para explorar, resumir e interpretar datos.

La mayoría de los análisis descriptivos que realiza un Data Analyst comienzan y terminan en Pandas.

Pandas permite responder preguntas como:

- ¿Cuántos registros existen?
- ¿Cuál es el promedio?
- ¿Cuál es la mediana?
- ¿Qué tan dispersos están los datos?
- ¿Existen valores atípicos?
- ¿Qué categorías dominan?
- ¿Qué variables están relacionadas?

---

# Mentalidad Correcta

Muchos principiantes creen que Pandas es solamente:

```python
read_csv()
```

o

```python
read_excel()
```

En realidad Pandas es una herramienta estadística.

Cada función responde una pregunta de negocio.

---

# Dataset de Ejemplo

```python
import pandas as pd

df = pd.DataFrame({
    "Edad":[25,30,28,40,35],
    "Salario":[5000,6500,6000,10000,7500],
    "Departamento":[
        "IT",
        "Finanzas",
        "IT",
        "Gerencia",
        "IT"
    ]
})
```

---

# 1. Conociendo el Dataset

## Ver Primeros Registros

```python
df.head()
```

Resultado:

```text
Edad  Salario  Departamento
25    5000     IT
30    6500     Finanzas
28    6000     IT
40   10000     Gerencia
35    7500     IT
```

---

## Ver Últimos Registros

```python
df.tail()
```

---

## Ver Dimensiones

```python
df.shape
```

Resultado:

```text
(5,3)
```

Interpretación:

```text
5 filas
3 columnas
```

---

## Ver Columnas

```python
df.columns
```

Resultado:

```text
Edad
Salario
Departamento
```

---

## Tipos de Datos

```python
df.dtypes
```

Resultado:

```text
Edad             int64
Salario          int64
Departamento    object
```

---

# 2. Información General

## Info()

```python
df.info()
```

---

Permite ver:

- Número de filas.
- Tipos de datos.
- Nulos.
- Uso de memoria.

---

Interpretación:

```text
Es el chequeo médico inicial
del dataset.
```

---

# 3. Estadística Descriptiva

## Describe()

```python
df.describe()
```

Resultado:

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

## ¿Qué Significa Cada Campo?

| Campo | Significado |
|---------|---------|
| count | Cantidad de registros |
| mean | Media |
| std | Desviación estándar |
| min | Valor mínimo |
| 25% | Q1 |
| 50% | Mediana |
| 75% | Q3 |
| max | Valor máximo |

---

# Ejemplo de Interpretación

```text
Salario

mean = 7000

50% = 6500
```

---

Interpretación:

```text
El salario promedio es 7000.

La mitad de empleados
ganan menos de 6500.
```

---

# 4. Medidas de Tendencia Central

## Media

Pregunta:

```text
¿Cuál es el promedio?
```

---

Código

```python
df["Salario"].mean()
```

---

Resultado

```text
7000
```

---

## Mediana

Pregunta:

```text
¿Cuál es el centro real?
```

---

Código

```python
df["Salario"].median()
```

---

Resultado

```text
6500
```

---

## Moda

Pregunta:

```text
¿Qué valor se repite más?
```

---

Código

```python
df["Departamento"].mode()
```

---

Resultado

```text
IT
```

---

# 5. Dispersión

## Desviación Estándar

Pregunta:

```text
¿Qué tan dispersos están los datos?
```

---

Código

```python
df["Salario"].std()
```

---

Interpretación

```text
Entre mayor sea el valor,
mayor dispersión existe.
```

---

## Varianza

```python
df["Salario"].var()
```

---

Interpretación

```text
Mide la dispersión al cuadrado.
```

---

## Rango

```python
df["Salario"].max() - df["Salario"].min()
```

---

Resultado

```text
5000
```

---

Interpretación

```text
Existe una diferencia
de 5000 entre el mayor y menor salario.
```

---

# 6. Percentiles y Cuartiles

## Cuartiles

```python
df["Salario"].quantile(0.25)

df["Salario"].quantile(0.50)

df["Salario"].quantile(0.75)
```

---

## Percentil 90

```python
df["Salario"].quantile(0.90)
```

---

Pregunta de Negocio

```text
¿Qué salario supera el 90%
de los empleados?
```

---

# 7. Valores Mínimos y Máximos

## Mínimo

```python
df["Salario"].min()
```

---

## Máximo

```python
df["Salario"].max()
```

---

Pregunta

```text
¿Cuál es el salario más alto?
```

---

# 8. Conteos

## Cantidad de Registros

```python
df["Salario"].count()
```

---

## Valores Únicos

```python
df["Departamento"].nunique()
```

---

Resultado

```text
3
```

---

Interpretación

```text
Existen tres departamentos.
```

---

# 9. Frecuencias

## Categorías

```python
df["Departamento"].value_counts()
```

Resultado

```text
IT          3
Finanzas    1
Gerencia    1
```

---

Interpretación

```text
IT domina el dataset.
```

---

## Porcentajes

```python
df["Departamento"]\
.value_counts(normalize=True)
```

---

Resultado

```text
IT          0.60
Finanzas    0.20
Gerencia    0.20
```

---

# 10. Valores Nulos

## Detección

```python
df.isnull().sum()
```

---

Resultado

```text
Edad            0
Salario         2
Departamento    0
```

---

Interpretación

```text
Existen 2 salarios faltantes.
```

---

# Porcentaje de Nulos

```python
(
 df.isnull().sum()
 /
 len(df)
)*100
```

---

# 11. Duplicados

## Detectar

```python
df.duplicated().sum()
```

---

## Eliminar

```python
df.drop_duplicates()
```

---

# 12. Filtrado Estadístico

## Salarios Altos

```python
df[df["Salario"] > 8000]
```

---

Pregunta

```text
¿Quién gana más de 8000?
```

---

## Múltiples Condiciones

```python
df[
    (df["Edad"] > 30)
    &
    (df["Salario"] > 7000)
]
```

---

# 13. Agrupaciones (Group By)

Una de las herramientas más poderosas.

---

Pregunta:

```text
¿Cuál es el salario promedio
por departamento?
```

---

Código

```python
df.groupby(
    "Departamento"
)["Salario"].mean()
```

---

Resultado

```text
IT           6166
Finanzas     6500
Gerencia    10000
```

---

# Múltiples Estadísticas

```python
df.groupby(
    "Departamento"
)["Salario"].agg(
    [
        "count",
        "mean",
        "median",
        "std",
        "min",
        "max"
    ]
)
```

---

# 14. Correlación

Pregunta:

```text
¿Qué variables se relacionan?
```

---

Código

```python
df.corr(numeric_only=True)
```

---

Resultado

```text
Edad vs Salario

0.75
```

---

Interpretación

```text
Relación positiva fuerte.
```

---

# 15. Outliers con IQR

## Cuartiles

```python
Q1 = df["Salario"].quantile(0.25)

Q3 = df["Salario"].quantile(0.75)
```

---

## IQR

```python
IQR = Q3 - Q1
```

---

## Límites

```python
inferior = Q1 - 1.5 * IQR

superior = Q3 + 1.5 * IQR
```

---

## Detectar Outliers

```python
df[
    (df["Salario"] < inferior)
    |
    (df["Salario"] > superior)
]
```

---

# 16. Tabla Dinámica (Pivot Table)

Pregunta:

```text
Resumen ejecutivo rápido.
```

---

Código

```python
pd.pivot_table(
    df,
    values="Salario",
    index="Departamento",
    aggfunc="mean"
)
```

---

# 17. Ranking

## Top Salarios

```python
df.sort_values(
    by="Salario",
    ascending=False
)
```

---

## Top 5

```python
df.nlargest(
    5,
    "Salario"
)
```

---

# 18. Pipeline Básico de EDA con Pandas

Cuando recibas un dataset:

```python
df.head()

df.shape

df.info()

df.describe()

df.isnull().sum()

df.duplicated().sum()

df.corr(
    numeric_only=True
)

df.value_counts()
```

---

# Flujo Mental de un Analista

```text
Dataset
   ↓
head()
   ↓
info()
   ↓
describe()
   ↓
nulos
   ↓
duplicados
   ↓
frecuencias
   ↓
groupby()
   ↓
correlaciones
   ↓
insights
```

---

# Mapa Mental de Pandas Estadístico

```text
PANDAS
│
├── Estructura
│   ├── head()
│   ├── shape
│   └── info()
│
├── Tendencia Central
│   ├── mean()
│   ├── median()
│   └── mode()
│
├── Dispersión
│   ├── std()
│   ├── var()
│   └── range
│
├── Posición
│   ├── quantile()
│   └── percentiles
│
├── Calidad
│   ├── isnull()
│   ├── duplicated()
│   └── nunique()
│
├── Agrupación
│   ├── groupby()
│   └── pivot_table()
│
├── Relación
│   └── corr()
│
└── Detección
    └── outliers
```

---

# Cheat Sheet Rápido

| Pregunta | Pandas |
|-----------|-----------|
| ¿Cuántas filas? | `df.shape` |
| ¿Qué columnas hay? | `df.columns` |
| ¿Qué tipos existen? | `df.info()` |
| ¿Promedio? | `mean()` |
| ¿Mediana? | `median()` |
| ¿Moda? | `mode()` |
| ¿Dispersión? | `std()` |
| ¿Cuartiles? | `quantile()` |
| ¿Frecuencias? | `value_counts()` |
| ¿Agrupaciones? | `groupby()` |
| ¿Correlación? | `corr()` |
| ¿Nulos? | `isnull().sum()` |
| ¿Duplicados? | `duplicated().sum()` |

---

# Regla de Oro

Si dominas estas funciones:

```python
head()
info()
describe()
mean()
median()
std()
quantile()
value_counts()
groupby()
corr()
```

podrás realizar aproximadamente el **80% del análisis descriptivo que se ejecuta diariamente en proyectos de Data Analytics, Power BI, Ciencia de Datos y Machine Learning**, porque estas funciones representan la traducción directa de los conceptos estadísticos fundamentales que has venido estudiando.
