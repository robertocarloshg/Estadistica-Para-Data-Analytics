# Glosario de Estadística para Data Analytics

> Documento de referencia rápida con los conceptos estadísticos más utilizados en análisis de datos, Python, Machine Learning y Business Intelligence.

---

# A

## Aleatorio (Random)

Proceso cuyo resultado no puede predecirse con certeza.

Ejemplo:
- Lanzar una moneda.
- Elegir un registro al azar de un dataset.

---

# B

## Big Data

Conjunto de datos tan grande o complejo que requiere tecnologías especiales para su procesamiento.

Características:
- Volumen
- Velocidad
- Variedad

---

# C

## Coeficiente de Correlación

Medida que indica qué tan relacionadas están dos variables.

Valores:
- +1 → relación positiva perfecta
- 0 → sin relación
- -1 → relación negativa perfecta

En Python:

```python
df["Ventas"].corr(df["Publicidad"])
```

---

## Cuartil

Valor que divide los datos en cuatro partes iguales.

- Q1 = 25%
- Q2 = 50% (mediana)
- Q3 = 75%

---

# D

## Data Analytics

Proceso de inspeccionar, transformar y modelar datos para obtener información útil.

---

## Dataset

Conjunto organizado de datos.

Ejemplo:

| Cliente | Edad | Salario |
|----------|--------|----------|
| Ana | 25 | 5000 |
| Luis | 40 | 8500 |

---

## Desviación Estándar

Medida de dispersión que indica cuánto se alejan los datos de la media.

Símbolo:
- σ (población)
- s (muestra)

Interpretación:

- Baja → datos agrupados
- Alta → datos dispersos

---

## Distribución Normal

Distribución de probabilidad con forma de campana.

Características:

- Media = Mediana = Moda
- Simétrica

Regla:

- 68% dentro de ±1σ
- 95% dentro de ±2σ
- 99.7% dentro de ±3σ

---

# E

## Error Estándar

Variabilidad del promedio muestral respecto a la media poblacional.

Fórmula:

SE = σ / √n

---

## Estadística

Rama de las matemáticas que estudia la recopilación, organización, análisis e interpretación de datos.

---

## Estadística Descriptiva

Resume y describe datos.

Ejemplos:

- Promedio
- Mediana
- Moda
- Histogramas

---

## Estadística Inferencial

Permite sacar conclusiones sobre una población utilizando una muestra.

Ejemplos:

- Intervalos de confianza
- Pruebas de hipótesis

---

# H

## Hipótesis

Afirmación que se desea comprobar mediante datos.

Tipos:

### Hipótesis Nula (H₀)

Indica que no existe diferencia o efecto.

### Hipótesis Alternativa (H₁)

Indica que sí existe diferencia o efecto.

---

## Histograma

Gráfico que muestra la distribución de una variable numérica mediante barras.

En Python:

```python
sns.histplot(df["Edad"])
```

---

# I

## Intervalo de Confianza

Rango donde se espera que se encuentre el parámetro poblacional con cierto nivel de confianza.

Ejemplo:

95% IC:

[48.5 , 52.1]

---

# M

## Media

Promedio aritmético.

Fórmula:

μ = Σx / n

Python:

```python
df["Ventas"].mean()
```

---

## Mediana

Valor central de un conjunto de datos ordenado.

Python:

```python
df["Ventas"].median()
```

---

## Moda

Valor que más se repite.

Python:

```python
df["Ventas"].mode()
```

---

## Muestreo

Proceso de seleccionar una parte de la población.

Tipos:

- Aleatorio simple
- Estratificado
- Sistemático
- Por conglomerados

---

## Muestra

Subconjunto de una población utilizado para realizar análisis.

Ejemplo:

- Población: 10,000 clientes
- Muestra: 500 clientes

---

# P

## Pandas

Biblioteca de Python para manipulación y análisis de datos.

Importación:

```python
import pandas as pd
```

---

## Percentil

Valor por debajo del cual se encuentra un porcentaje determinado de observaciones.

Ejemplo:

- Percentil 90 → 90% de los datos quedan debajo.

---

## p-value

Probabilidad de obtener un resultado igual o más extremo si la hipótesis nula es verdadera.

Regla común:

- p < 0.05 → rechazar H₀
- p ≥ 0.05 → no rechazar H₀

---

## Población

Conjunto completo de elementos que se desean estudiar.

Ejemplo:

Todos los clientes de un banco.

---

## Probabilidad

Medida de la posibilidad de que ocurra un evento.

Rango:

0 ≤ P ≤ 1

---

# R

## Rango

Diferencia entre el valor máximo y mínimo.

Fórmula:

Rango = Máximo - Mínimo

---

## Regresión

Método estadístico para modelar relaciones entre variables.

Ejemplo:

Predecir ventas utilizando inversión en publicidad.

---

# S

## Sesgo (Bias)

Error sistemático que afecta los resultados de un estudio o modelo.

Ejemplos:

- Muestreo incorrecto
- Datos incompletos

---

## Skewness (Asimetría)

Mide la inclinación de una distribución.

Tipos:

- Positiva
- Negativa
- Simétrica

Python:

```python
df["Ventas"].skew()
```

---

# V

## Variable

Característica que puede tomar distintos valores.

Ejemplos:

- Edad
- Salario
- Ciudad

---

## Variable Categórica

Representa categorías o grupos.

Ejemplos:

- Género
- Departamento
- País

---

## Variable Numérica

Representa cantidades medibles.

Ejemplos:

- Edad
- Peso
- Salario

---

## Varianza

Medida de dispersión basada en las diferencias cuadráticas respecto a la media.

Fórmula:

σ² = Σ(x − μ)² / N

Python:

```python
df["Ventas"].var()
```

---

# Resumen de Conceptos Fundamentales

| Concepto | Pregunta que responde |
|-----------|-----------------------|
| Media | ¿Cuál es el promedio? |
| Mediana | ¿Cuál es el valor central? |
| Moda | ¿Qué valor se repite más? |
| Varianza | ¿Qué tan dispersos están los datos? |
| Desviación estándar | ¿Cuánto se alejan del promedio? |
| Correlación | ¿Hay relación entre variables? |
| Probabilidad | ¿Qué tan probable es un evento? |
| p-value | ¿Existe evidencia estadística? |
| Intervalo de confianza | ¿Cuál es el rango probable? |
| Muestreo | ¿Cómo selecciono datos? |

---

# Ruta de Aprendizaje Recomendada

1. Población y Muestra
2. Tipos de Variables
3. Media, Mediana y Moda
4. Varianza y Desviación Estándar
5. Cuartiles y Percentiles
6. Histogramas y Boxplots
7. Probabilidad
8. Distribución Normal
9. Muestreo
10. Intervalos de Confianza
11. Hipótesis y p-value
12. Correlación
13. EDA
14. Pandas Estadístico

---

Fin del Curso Base de Estadística para Data Analytics con Python.
