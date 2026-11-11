# Histogramas y BoxPlots

## Objetivo

Los histogramas y boxplots permiten visualizar la distribución de los datos.

Antes de calcular modelos, correlaciones o predicciones, debes entender:

- Cómo se distribuyen los datos.
- Dónde se concentran.
- Si existen valores atípicos.
- Si la distribución es simétrica o sesgada.
- Si existen varios grupos dentro de la misma variable.

---

# ¿Por qué son importantes?

Las medidas estadísticas por sí solas pueden ocultar información.

Por ejemplo:

```text
Media = 50
```

Dos conjuntos pueden tener exactamente la misma media pero distribuciones completamente diferentes.

---

## Dataset A

```text
48
49
50
51
52
```

---

## Dataset B

```text
10
20
50
80
90
```

---

Aunque ambos tienen una media similar, su comportamiento es muy distinto.

Por eso se utilizan gráficos.

---

# Histograma

## Definición

Un histograma muestra la frecuencia de los datos agrupados en intervalos (bins).

Permite observar cómo se distribuyen los valores.

---

# Ejemplo

Ventas diarias:

```text
10
12
15
20
22
25
26
30
31
35
40
```

---

## Histograma Simplificado

```text
10 - 19   ███

20 - 29   █████

30 - 39   ███

40 - 49   █
```

---

## Componentes

### Eje X

Representa los valores.

```text
Salario
Edad
Ventas
Tiempo
Temperatura
```

---

### Eje Y

Representa la frecuencia.

```text
Cantidad de veces que aparece cada rango
```

---

# ¿Qué información nos da?

## Concentración

Permite identificar dónde se agrupan los datos.

```text
██
████
██████████
████
██
```

Interpretación:

La mayoría de observaciones se concentra en el centro.

---

## Dispersión

Permite observar qué tan extendidos están los datos.

```text
█ █ █ █ █ █ █ █
```

Interpretación:

Los datos están muy dispersos.

---

## Asimetría

Permite detectar sesgos.

---

### Asimetría Positiva

Cola hacia la derecha.

```text
█████████
██████
████
██
█
```

Interpretación:

Pocos valores muy altos arrastran la distribución.

Ejemplos:

- Salarios
- Patrimonio
- Ventas

---

### Asimetría Negativa

Cola hacia la izquierda.

```text
█
██
████
██████
█████████
```

Interpretación:

Existen pocos valores extremadamente bajos.

---

### Simétrica

```text
    █
   ███
  █████
 ███████
█████████
 ███████
  █████
   ███
    █
```

Interpretación:

Media ≈ Mediana ≈ Moda

---

# Distribuciones Multimodales

Una distribución puede tener múltiples grupos.

Ejemplo:

```text
███
██████

      ██████
       ████
```

Interpretación:

Podrían existir dos tipos de clientes.

Por ejemplo:

- Clientes individuales.
- Clientes corporativos.

---

# BoxPlot

## Definición

Un boxplot resume una distribución utilizando:

```text
Mínimo
Q1
Mediana
Q3
Máximo
Outliers
```

---

# Estructura

```text
          ●

|------|======|------|
       |
    Mediana
```

---

## Componentes

### Caja

Representa el 50% central de los datos.

```text
Q1 -------- Q3
```

---

### Línea central

Representa la mediana.

```text
Q2
```

---

### Bigotes

Representan los límites normales de la distribución.

```text
Min -------- Max
```

---

### Puntos aislados

Representan posibles outliers.

```text
●
```

---

# Ejemplo

Datos:

```text
10
15
20
25
30
35
40
45
50
200
```

---

Boxplot:

```text
                    ●

|------|======|------|
```

Interpretación:

```text
200 es sospechoso
```

Debe revisarse.

---

# Comparación Histograma vs BoxPlot

## Histograma

Muestra forma y distribución.

```text
████
██████
████████
████
██
```

Permite ver:

- Concentración
- Asimetría
- Patrones
- Agrupaciones

---

## BoxPlot

Resume la distribución.

```text
|----|=====|----|
```

Permite ver:

- Mediana
- Cuartiles
- Dispersión
- Outliers

---

# Cuándo usar cada uno

| Situación | Histograma | BoxPlot |
|------------|------------|------------|
| Ver distribución completa | ✅ | ❌ |
| Detectar outliers | ⚠️ | ✅ |
| Comparar grupos | ⚠️ | ✅ |
| Analizar forma | ✅ | ❌ |
| Detectar asimetrías | ✅ | ✅ |

---

# Ejemplo de Negocio

## Salarios

Histograma

```text
Q3,000 - Q5,000      ███████████

Q5,000 - Q7,000      ████████

Q7,000 - Q10,000     ███

Q10,000+             █
```

Interpretación:

La mayoría de empleados gana entre Q3,000 y Q7,000.

---

## Con BoxPlot

```text
                     ● 25000

|------|======|------|
```

Interpretación:

Existe un salario extraordinariamente alto.

Posibles causas:

- Gerencia.
- Director.
- Dato incorrecto.

---

# Interpretación de la Mediana en el BoxPlot

## Caso 1

```text
|---|===|---|
      |
```

La mediana está centrada.

Interpretación:

Distribución aproximadamente simétrica.

---

## Caso 2

```text
|--|===|------|
    |
```

Interpretación:

Sesgo hacia la derecha.

---

## Caso 3

```text
|------|===|--|
           |
```

Interpretación:

Sesgo hacia la izquierda.

---

# Histogramas y Distribución Normal

Cuando los datos siguen una distribución normal, el histograma tiene forma de campana.

```text
       █
      ███
     █████
   █████████
 █████████████
   █████████
     █████
      ███
       █
```

Interpretación:

- La mayoría de observaciones están cerca de la media.
- Pocos valores se encuentran en los extremos.

---

# En Python (Matplotlib)

## Histograma

```python
import matplotlib.pyplot as plt

plt.hist(df["Salario"])
plt.show()
```

---

## Definir Número de Bins

```python
plt.hist(df["Salario"], bins=20)
plt.show()
```

---

# En Seaborn

## Histograma

```python
import seaborn as sns

sns.histplot(df["Salario"])
```

---

## Histograma con Curva de Densidad

```python
sns.histplot(
    df["Salario"],
    kde=True
)
```

---

Resultado:

```text
Histograma
+
Curva de distribución
```

---

# BoxPlot en Seaborn

```python
sns.boxplot(
    x=df["Salario"]
)
```

---

## Comparar Departamentos

```python
sns.boxplot(
    x="Departamento",
    y="Salario",
    data=df
)
```

---

Interpretación:

Permite comparar:

- Medianas.
- Dispersión.
- Outliers.

Entre distintos grupos.

---

# En Pandas

## Histograma

```python
df["Salario"].hist()
```

---

## BoxPlot

```python
df.boxplot(column="Salario")
```

---

# Relación con EDA

Al recibir un dataset nuevo:

```python
df.info()
df.describe()
```

Después:

```python
sns.histplot()
sns.boxplot()
```

---

¿Por qué?

Porque revelarás inmediatamente:

- Distribuciones extrañas.
- Datos faltantes.
- Posibles errores.
- Outliers.
- Sesgos.
- Concentraciones.

---

# Casos Típicos de Uso

## Análisis de Clientes

Variable:

```text
Edad
```

Objetivo:

```text
Ver distribución de edades.
```

Herramienta:

```text
Histograma
```

---

## Salarios

Objetivo:

```text
Detectar salarios atípicos.
```

Herramienta:

```text
BoxPlot
```

---

## Riesgo Operacional

Variable:

```text
Días de resolución.
```

Objetivo:

```text
Evaluar dispersión y demoras excesivas.
```

Herramienta:

```text
Histograma + BoxPlot
```

---

# Preguntas que responde un Histograma

- ¿Cómo se distribuyen los datos?
- ¿Son simétricos?
- ¿Hay varios grupos?
- ¿Dónde se concentran?
- ¿Existe una distribución normal?

---

# Preguntas que responde un BoxPlot

- ¿Cuál es la mediana?
- ¿Dónde están los cuartiles?
- ¿Hay valores atípicos?
- ¿Qué tan dispersos están los datos?
- ¿Cómo comparar varios grupos rápidamente?

---

# Cheat Sheet Rápido

| Concepto | Utilidad |
|----------|----------|
| Histograma | Ver distribución |
| Bin | Intervalo del histograma |
| Frecuencia | Cantidad de observaciones |
| BoxPlot | Resumen estadístico visual |
| Mediana | Línea central de la caja |
| Q1 | Inicio de la caja |
| Q3 | Fin de la caja |
| IQR | Q3 - Q1 |
| Outlier | Punto fuera de los límites normales |

---

# Regla para Data Analytics

Cuando recibas cualquier dataset:

```python
sns.histplot(variable, kde=True)
sns.boxplot(x=variable)
```

Con solo estos dos gráficos podrás responder:

✅ ¿Cómo se distribuyen los datos?

✅ ¿Existen outliers?

✅ ¿Es una distribución normal?

✅ ¿Hay sesgo?

✅ ¿Existen grupos ocultos?

✅ ¿La media es realmente representativa?

Antes de construir cualquier modelo, estos dos gráficos deberían ser obligatorios en tu EDA.
