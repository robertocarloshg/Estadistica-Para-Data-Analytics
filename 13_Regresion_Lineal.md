# Regresión Lineal

## Objetivo

La regresión lineal permite modelar y predecir una variable utilizando otra variable relacionada.

Responde preguntas como:

- ¿Cómo afecta la experiencia al salario?
- ¿Cuánto aumentan las ventas por cada dólar invertido en publicidad?
- ¿Cómo cambia el tiempo de atención según la complejidad de un caso?
- ¿Puedo predecir un valor futuro?

---

# ¿Qué es una Regresión?

La regresión busca encontrar una ecuación matemática que describa la relación entre variables.

Mientras la correlación responde:

```text
¿Existe relación?
```

La regresión responde:

```text
¿Cuánto cambia Y cuando cambia X?
```

---

# Ejemplo

Supongamos:

| Horas Estudiadas | Nota |
|------------------|------|
| 1 | 50 |
| 2 | 55 |
| 3 | 60 |
| 4 | 65 |
| 5 | 70 |

Podemos observar:

```text
Más horas de estudio
→ Mejor nota
```

---

# Variable Dependiente e Independiente

## Variable Independiente (X)

Es la variable explicativa.

También se conoce como:

```text
Predictor
Feature
Variable explicativa
```

Ejemplos:

```text
Horas estudiadas
Inversión en publicidad
Edad
Experiencia
```

---

## Variable Dependiente (Y)

Es la variable que deseamos explicar o predecir.

También se conoce como:

```text
Variable objetivo
Target
Respuesta
```

Ejemplos:

```text
Nota
Ventas
Salario
Tiempo de resolución
```

---

# Ejemplo Visual

```text
Horas Estudio (X)
         ↓
      Influye
         ↓
      Nota (Y)
```

---

# Ecuación de la Regresión Lineal

La forma básica es:

```text
Y = a + bX
```

---

Donde:

| Parámetro | Significado |
|------------|------------|
| Y | Valor a predecir |
| X | Variable explicativa |
| a | Intercepto |
| b | Pendiente |

---

# Intercepto (a)

Es el valor de Y cuando X vale cero.

---

Ejemplo:

```text
Nota = 40 + 5(Horas)
```

Si:

```text
Horas = 0
```

Entonces:

```text
Nota = 40
```

---

Interpretación:

```text
Sin estudiar,
la nota esperada sería 40.
```

---

# Pendiente (b)

Indica cuánto cambia Y cuando X aumenta una unidad.

---

Ejemplo:

```text
Nota = 40 + 5(Horas)
```

Pendiente:

```text
5
```

Interpretación:

```text
Cada hora adicional
incrementa aproximadamente
5 puntos en la nota.
```

---

# Predicción

Usando:

```text
Nota = 40 + 5(Horas)
```

Si un alumno estudia:

```text
6 horas
```

---

Resultado:

```text
Nota = 40 + 5(6)

Nota = 70
```

---

# Representación Gráfica

Datos observados:

```text
                  ●

              ●

          ●

      ●

  ●
```

---

Regresión:

```text
                  ●

              ●

          ●

      ●

  ●

 ──────────────────
 Línea de Regresión
```

---

# ¿Cómo Encuentra la Línea Correcta?

La regresión intenta minimizar los errores.

---

# Error (Residuo)

Es la diferencia entre:

```text
Valor real
```

y

```text
Valor predicho
```

---

Ejemplo

```text
Nota real = 80

Nota predicha = 75
```

---

Error

```text
80 - 75 = 5
```

---

# Residuos

## Definición

Errores de predicción.

---

Visualmente:

```text
      ● real

      │
      │ error
      │

──────┼──────
 Línea
```

---

Una buena regresión tiene residuos pequeños.

---

# Método de Mínimos Cuadrados

La técnica más utilizada.

Busca minimizar:

```text
Σ(error²)
```

---

¿Por qué elevar al cuadrado?

- Evita errores negativos.
- Penaliza errores grandes.

---

# Coeficiente de Determinación (R²)

Una de las métricas más importantes.

---

## Pregunta que responde

```text
¿Qué porcentaje de la variación
de Y es explicado por X?
```

---

# Escala

```text
0 ≤ R² ≤ 1
```

---

# Interpretación

## R² = 0

```text
No explica nada.
```

---

## R² = 0.50

```text
Explica el 50%
de la variabilidad.
```

---

## R² = 0.90

```text
Explica el 90%
de la variabilidad.
```

---

## R² = 1

```text
Predicción perfecta.
```

---

# Ejemplo

Relación:

```text
Experiencia → Salario
```

Resultado:

```text
R² = 0.84
```

Interpretación:

```text
El 84% de la variación
del salario se explica
por la experiencia.
```

---

# Correlación vs Regresión

| Aspecto | Correlación | Regresión |
|----------|----------|----------|
| Relación | Sí | Sí |
| Predicción | No | Sí |
| Dirección | No | Sí |
| Fórmula | No | Sí |
| Variable dependiente | No | Sí |

---

# Ejemplo

Correlación:

```text
r = 0.80
```

Solo informa:

```text
Existe relación fuerte.
```

---

Regresión:

```text
Salario = 2000 + 500(AñosExperiencia)
```

Permite estimar:

```text
Salario futuro.
```

---

# Supuestos de la Regresión Lineal

## 1. Relación Lineal

Debe existir una tendencia aproximadamente lineal.

---

Correcto:

```text
      ●
    ●
  ●
●
```

---

Incorrecto:

```text
●
  ●
      ●
          ●●●
```

---

# 2. Independencia

Las observaciones no deben depender unas de otras.

---

# 3. Homocedasticidad

La dispersión de errores debe ser similar.

---

Bueno:

```text
   ●
   ●
   ●
   ●
```

---

Problema:

```text
●

  ●●

      ●●●●

            ●●●●●●
```

---

# 4. Residuos Aproximadamente Normales

Los errores deberían parecer una distribución normal.

---

# Ejemplo de Negocio

## Experiencia y Salario

Datos:

| Experiencia | Salario |
|------------|---------|
| 1 | 2500 |
| 2 | 3000 |
| 3 | 3500 |
| 4 | 4000 |
| 5 | 4500 |

---

Modelo:

```text
Salario = 2000 + 500(X)
```

---

Interpretación

```text
Cada año adicional
incrementa aproximadamente
Q500 de salario.
```

---

# Ejemplo en Riesgo Operacional

Variables:

```text
Complejidad
Tiempo Resolución
```

---

Resultado:

```text
Tiempo = 2 + 1.8(Complejidad)
```

---

Interpretación:

```text
Cada nivel adicional
de complejidad incrementa
1.8 días de resolución.
```

---

# Regresión Múltiple

No siempre existe una sola variable.

---

Ecuación:

```text
Y = a + b1X1 + b2X2 + b3X3
```

---

Ejemplo

```text
Salario =
2000
+ 500(Experiencia)
+ 300(Certificaciones)
+ 150(Educación)
```

---

Aquí:

```text
Experiencia
Certificaciones
Educación
```

contribuyen al salario.

---

# En Python (Scikit-Learn)

## Importar

```python
from sklearn.linear_model import LinearRegression
```

---

# Variables

```python
X = df[["HorasEstudio"]]

y = df["Nota"]
```

---

# Modelo

```python
modelo = LinearRegression()

modelo.fit(X, y)
```

---

# Coeficientes

## Pendiente

```python
modelo.coef_
```

---

## Intercepto

```python
modelo.intercept_
```

---

# Predicción

```python
modelo.predict([[6]])
```

---

Resultado:

```text
Nota estimada para 6 horas.
```

---

# R²

```python
modelo.score(X, y)
```

---

Resultado:

```text
0.85
```

---

Interpretación:

```text
85% explicado por el modelo.
```

---

# Visualización

## Scatter Plot

```python
sns.scatterplot(
    x="HorasEstudio",
    y="Nota",
    data=df
)
```

---

## Línea de Regresión

```python
sns.regplot(
    x="HorasEstudio",
    y="Nota",
    data=df
)
```

---

# Relación con Machine Learning

La regresión lineal es uno de los algoritmos más simples y utilizados.

También es la puerta de entrada a:

```text
Machine Learning
      ↓
Regresión Múltiple
      ↓
Regularización
      ↓
Random Forest
      ↓
Gradient Boosting
```

---

# Preguntas que Responde

- ¿Existe una relación cuantificable?
- ¿Cuánto cambia Y cuando cambia X?
- ¿Puedo predecir valores?
- ¿Qué variable tiene mayor impacto?
- ¿Qué tan bueno es mi modelo?

---

# Cheat Sheet Rápido

| Concepto | Significado |
|-----------|-----------|
| X | Variable independiente |
| Y | Variable dependiente |
| Intercepto (a) | Valor inicial |
| Pendiente (b) | Cambio por unidad |
| Residuo | Error de predicción |
| R² | Variabilidad explicada |
| Regresión | Predicción |
| Correlación | Asociación |

---

# Flujo Mental

```text
Correlación
      ↓
¿Existe relación?
      ↓
Sí
      ↓
Regresión
      ↓
Obtener ecuación
      ↓
Medir R²
      ↓
Realizar predicciones
```

---

# Regla para Data Analytics

Cuando encuentres una correlación interesante:

```text
Edad ↔ Salario

Experiencia ↔ Ventas

Complejidad ↔ Tiempo
```

No te detengas ahí.

Da el siguiente paso:

```text
Construye una regresión.
```

Porque la correlación te dice que existe una relación, pero la regresión te permite **medirla, explicarla y utilizarla para realizar predicciones**, que es donde comienza el verdadero valor analítico.
