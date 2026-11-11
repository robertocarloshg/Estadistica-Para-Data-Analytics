# Distribución Normal

## Objetivo

La distribución normal es una de las herramientas más importantes de la estadística.

Permite describir cómo se comportan muchas variables del mundo real y constituye la base de gran parte de la estadística inferencial, Machine Learning y Ciencia de Datos.

Responde preguntas como:

- ¿Qué tan común o raro es un valor?
- ¿Qué porcentaje de observaciones está dentro de un rango?
- ¿Es este dato un caso atípico?
- ¿Esta medición está dentro de lo esperado?

---

# ¿Qué es una Distribución Normal?

Es una distribución de probabilidad con forma de campana simétrica.

También se conoce como:

```text
Campana de Gauss
Distribución Gaussiana
```

Su característica principal es que la mayoría de los datos se concentran cerca del centro y cada vez hay menos datos conforme nos alejamos de él.

---

# Forma de la Distribución

```text
                    █
                 ███████
              █████████████
           ███████████████████
        █████████████████████████
     ███████████████████████████████
        █████████████████████████
           ███████████████████
              █████████████
                 ███████
                    █
```

---

# Ejemplo Real

Altura de personas adultas:

```text
150 cm
160 cm
170 cm
180 cm
190 cm
```

La mayoría se concentra alrededor de:

```text
170 cm
```

Hay pocas personas extremadamente bajas o extremadamente altas.

---

# Características Principales

## Simetría

La distribución es perfectamente simétrica.

```text
Izquierda = Derecha
```

---

## Media = Mediana = Moda

En una distribución normal:

```text
Media = Mediana = Moda
```

Visualmente:

```text
               |
               |
               |
          MEDIA
         MEDIANA
           MODA
```

Las tres medidas coinciden en el centro.

---

## Datos Concentrados en el Centro

La mayoría de observaciones se encuentran cerca de la media.

Mientras más te alejes del centro:

```text
Menos frecuentes son los datos.
```

---

# Parámetros de la Distribución Normal

Se describe mediante dos valores:

---

## Media (μ)

Representa el centro de la distribución.

Ejemplo:

```text
μ = 70
```

---

## Desviación Estándar (σ)

Indica qué tan dispersos están los datos.

Ejemplo:

```text
σ = 10
```

---

# Ejemplo Completo

Supongamos un examen.

```text
Media = 70 puntos
Desviación = 10 puntos
```

---

Distribución:

```text
40 50 60 70 80 90 100

      ▲
      70
```

---

Interpretación:

```text
La mayoría de alumnos obtuvieron notas cercanas a 70.
```

---

# Regla Empírica (68 - 95 - 99.7)

La mayor parte de los análisis iniciales se realizan usando esta regla.

---

## ±1 Desviación Estándar

```text
68%
```

de los datos se encuentran dentro de:

```text
μ ± 1σ
```

---

Ejemplo:

```text
μ = 70
σ = 10
```

```text
60 a 80
```

Contiene aproximadamente:

```text
68% de los alumnos
```

---

## ±2 Desviaciones Estándar

```text
95%
```

de los datos se encuentran dentro de:

```text
μ ± 2σ
```

---

Ejemplo

```text
50 a 90
```

Contiene aproximadamente:

```text
95% de los alumnos
```

---

## ±3 Desviaciones Estándar

```text
99.7%
```

de los datos se encuentran dentro de:

```text
μ ± 3σ
```

---

Ejemplo

```text
40 a 100
```

Contiene aproximadamente:

```text
99.7% de los alumnos
```

---

# Visualización

```text
                  μ
                  ▼

    -3σ   -2σ   -1σ     +1σ   +2σ   +3σ

-----|-----|-----|-----|-----|-----|-----

 0.15% 2.35% 13.5% 34% 34% 13.5% 2.35% 0.15%
```

---

# Interpretación Práctica

Supongamos:

```text
Salario promedio: Q8,000
Desviación estándar: Q1,000
```

---

Empleado A

```text
Q8,500
```

Interpretación:

```text
Salario normal.
```

---

Empleado B

```text
Q15,000
```

Interpretación:

```text
Muy poco común.
```

Probablemente se encuentra fuera de 3 desviaciones estándar.

---

# Z-Score

## Definición

Permite saber cuántas desviaciones estándar se encuentra un dato respecto a la media.

---

## Fórmula

```text
Z = (X - μ) / σ
```

Donde:

```text
X = valor observado
μ = media
σ = desviación estándar
```

---

# Ejemplo

```text
Media = 70
Desviación = 10

Alumno = 90
```

---

Cálculo

```text
Z = (90 - 70) / 10

Z = 2
```

---

Interpretación

```text
El alumno está 2 desviaciones estándar
por encima de la media.
```

---

# ¿Cuándo un Z-Score es Sospechoso?

Regla común:

| Z-Score | Interpretación |
|----------|----------|
| 0 | Promedio |
| ±1 | Normal |
| ±2 | Poco común |
| ±3 o más | Muy inusual |

---

Ejemplo

```text
Z = 3.5
```

Posible:

```text
Outlier
```

---

# Distribución Normal y Outliers

Valores muy alejados del promedio son extremadamente raros.

---

Ejemplo

```text
Media = 100
σ = 15
```

---

Valor:

```text
160
```

---

Cálculo

```text
Z = (160 - 100) / 15

Z = 4
```

Resultado:

```text
Probablemente un outlier.
```

---

# Ejemplos Reales de Variables Aproximadamente Normales

## Altura

```text
Personas adultas
```

---

## Peso

```text
Poblaciones homogéneas
```

---

## Calificaciones

```text
Exámenes masivos
```

---

## Errores de Medición

```text
Sensores
Instrumentos
```

---

# Variables que NO suelen ser Normales

## Salarios

Generalmente tienen sesgo positivo.

```text
Muchos ganan poco
Pocos ganan muchísimo
```

---

## Ventas

```text
Muchos clientes compran poco
Pocos clientes compran mucho
```

---

## Patrimonio

```text
Distribución muy asimétrica
```

---

# Histograma de una Distribución Normal

```text
sns.histplot(
    variable,
    kde=True
)
```

Resultado esperado:

```text
       █
      ███
    ███████
  ███████████
███████████████
  ███████████
    ███████
      ███
       █
```

---

# Cómo Detectar una Distribución Aproximadamente Normal

## Señal 1

Media y mediana similares.

```text
Media ≈ Mediana
```

---

## Señal 2

Histograma simétrico.

---

## Señal 3

Pocos outliers.

---

## Señal 4

Forma de campana.

---

# Importancia para Data Analytics

Muchas técnicas asumen normalidad.

Por ejemplo:

- Intervalos de confianza.
- Pruebas de hipótesis.
- Regresión lineal.
- ANOVA.
- Control estadístico de procesos.

---

# En Python (NumPy)

## Media

```python
np.mean(datos)
```

---

## Desviación Estándar

```python
np.std(datos)
```

---

## Z-Score

```python
from scipy.stats import zscore

zscore(datos)
```

---

# En Pandas

## Media

```python
df["Salario"].mean()
```

---

## Desviación

```python
df["Salario"].std()
```

---

## Histograma

```python
df["Salario"].hist()
```

---

# En Seaborn

## Histograma con Curva

```python
import seaborn as sns

sns.histplot(
    df["Salario"],
    kde=True
)
```

---

# Aplicación en Negocio

## Riesgo Operacional

Tiempo promedio de resolución:

```text
Media = 8 días
σ = 2 días
```

---

Caso:

```text
18 días
```

---

Interpretación:

```text
Muy alejado de lo normal.
```

Debe investigarse.

---

## Ventas

```text
Media = Q30,000
σ = Q5,000
```

---

Vendedor:

```text
Q45,000
```

---

Cálculo:

```text
Z = 3
```

Interpretación:

```text
Desempeño excepcional.
```

---

# Relación con Temas Anteriores

```text
Media
   ↓
Desviación Estándar
   ↓
Distribución Normal
   ↓
Z-Score
   ↓
Percentiles
   ↓
Intervalos de Confianza
   ↓
Hipótesis Estadísticas
```

La distribución normal es el puente entre la estadística descriptiva y la estadística inferencial.

---

# Preguntas que Responde

- ¿Qué tan común es un valor?
- ¿Qué valores son inusuales?
- ¿La distribución es simétrica?
- ¿Qué porcentaje de datos está cerca de la media?
- ¿Existen posibles outliers?
- ¿Puedo aplicar ciertos métodos estadísticos?

---

# Cheat Sheet Rápido

| Concepto | Significado |
|----------|----------|
| μ | Media |
| σ | Desviación estándar |
| Normal | Distribución tipo campana |
| Z-Score | Distancia respecto a la media |
| 68% | Dentro de ±1σ |
| 95% | Dentro de ±2σ |
| 99.7% | Dentro de ±3σ |
| Z > 3 | Posible outlier |
| Media ≈ Mediana ≈ Moda | Señal de normalidad |

---

# Regla para Data Analytics

Cuando recibas una variable numérica:

```python
df["variable"].describe()

sns.histplot(
    df["variable"],
    kde=True
)
```

Pregúntate:

✅ ¿Tiene forma de campana?

✅ ¿Media y mediana son parecidas?

✅ ¿Existen valores extremos?

✅ ¿La desviación estándar es razonable?

✅ ¿Pueden calcularse z-scores?

Si respondes estas preguntas, ya estás pensando como un analista y no solamente como alguien que ejecuta código.
