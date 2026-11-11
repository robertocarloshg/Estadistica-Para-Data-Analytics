# Correlación

## Objetivo

La correlación mide la fuerza y dirección de la relación entre dos variables.

Responde preguntas como:

- ¿A mayor experiencia laboral aumenta el salario?
- ¿A más horas de estudio mejor calificación?
- ¿A mayor temperatura aumentan las ventas de helado?
- ¿Existe relación entre dos variables?

---

# Concepto Fundamental

La correlación indica cómo cambian dos variables entre sí.

Si una variable cambia, queremos saber:

```text
¿Qué ocurre con la otra?
```

---

# Ejemplo

Supongamos:

| Horas de Estudio | Nota |
|-----------------|-------|
| 2 | 60 |
| 3 | 65 |
| 4 | 70 |
| 5 | 80 |
| 6 | 90 |

Observación:

```text
Más horas de estudio
↓
Mayores notas
```

Existe correlación positiva.

---

# Tipos de Correlación

## Correlación Positiva

Cuando ambas variables aumentan juntas.

---

### Ejemplo

```text
Horas de estudio ↑
Notas ↑
```

Visualmente:

```text
          ●
        ●
      ●
    ●
  ●
```

---

Interpretación:

```text
Cuando una aumenta,
la otra también tiende a aumentar.
```

---

## Correlación Negativa

Cuando una aumenta y la otra disminuye.

---

### Ejemplo

```text
Horas viendo televisión ↑
Calificaciones ↓
```

Visualmente:

```text
●
  ●
     ●
        ●
           ●
```

---

Interpretación:

```text
Cuando una aumenta,
la otra disminuye.
```

---

## Correlación Nula

No existe relación observable.

---

Ejemplo:

```text
Número de zapatos
Calificación universitaria
```

Visualmente:

```text
 ●      ●

      ●

●          ●

    ●
```

---

Interpretación:

```text
No parece existir relación.
```

---

# Coeficiente de Correlación

El valor más utilizado es:

```text
Coeficiente de Pearson (r)
```

---

# Rango de Valores

```text
-1 ≤ r ≤ 1
```

---

Visualización:

```text
-1 -------- 0 -------- +1
```

---

# Significado

## r = +1

Correlación positiva perfecta.

```text
X aumenta
Y aumenta
```

Siempre.

---

## r = -1

Correlación negativa perfecta.

```text
X aumenta
Y disminuye
```

Siempre.

---

## r = 0

No existe relación lineal.

---

# Escala Práctica

| Correlación | Interpretación |
|-------------|---------------|
| 0.00 - 0.19 | Muy débil |
| 0.20 - 0.39 | Débil |
| 0.40 - 0.59 | Moderada |
| 0.60 - 0.79 | Fuerte |
| 0.80 - 1.00 | Muy fuerte |

*La misma lógica aplica para valores negativos.*

---

# Ejemplos de Interpretación

## r = 0.85

```text
Correlación positiva muy fuerte
```

Ejemplo:

```text
Horas trabajadas
Ingresos por comisión
```

---

## r = -0.72

```text
Correlación negativa fuerte
```

Ejemplo:

```text
Velocidad de respuesta
Tiempo total de atención
```

---

## r = 0.05

```text
Correlación prácticamente inexistente
```

---

# Scatter Plot

La forma más común de visualizar correlaciones.

---

## Correlación Positiva

```text
          ●
        ●
      ●
    ●
  ●
```

---

## Correlación Negativa

```text
●
  ●
     ●
        ●
           ●
```

---

## Correlación Débil

```text
●      ●

      ●

  ●

        ●
```

---

## Sin Correlación

```text
●    ●      ●

    ●

      ●

●         ●
```

---

# Correlación NO Implica Causalidad

Este es uno de los conceptos más importantes de toda la estadística.

---

## Correlación

Indica asociación.

```text
Dos variables se mueven juntas.
```

---

## Causalidad

Indica que una variable provoca cambios en otra.

```text
X causa Y
```

---

# Ejemplo Clásico

Existe correlación entre:

```text
Ventas de helados
Ahogamientos en piscinas
```

---

¿Los helados provocan ahogamientos?

```text
NO
```

---

Variable oculta:

```text
Temperatura
```

---

Cuando hace calor:

```text
Más helados
Más personas nadando
Más accidentes
```

---

# Variable Confusora

Una variable externa que influye en ambas.

---

Visualización

```text
Temperatura
     ↓
Helados

Temperatura
     ↓
Ahogamientos
```

---

# Correlación vs Causalidad

| Situación | Correlación | Causalidad |
|------------|------------|------------|
| Horas de estudio y nota | ✅ | Probable |
| Altura y peso | ✅ | Relacionadas |
| Helados y ahogamientos | ✅ | ❌ |
| Edad y salario | ✅ | Parcial |

---

# Correlación de Pearson

## Cuándo usarla

Variables numéricas.

Ejemplos:

```text
Edad
Salario
Ventas
Tiempo
Producción
```

---

Supone:

- Relación lineal.
- Variables numéricas.
- Pocos outliers extremos.

---

# Correlación de Spearman

## Cuándo usarla

Cuando los datos no son normales o contienen rankings.

---

Ejemplo

```text
Posición en ventas
Ranking académico
Nivel de riesgo
```

---

Mide:

```text
Relaciones monotónicas
```

No necesariamente lineales.

---

# Pearson vs Spearman

| Característica | Pearson | Spearman |
|----------------|----------|----------|
| Datos numéricos | ✅ | ✅ |
| Relaciones lineales | ✅ | ⚠️ |
| Rankings | ❌ | ✅ |
| Resistente a Outliers | ❌ | Más resistente |

---

# Matriz de Correlación

Cuando existen múltiples variables.

---

Ejemplo

| Variable | Edad | Salario | Experiencia |
|-----------|--------|--------|--------|
| Edad | 1.00 | 0.50 | 0.85 |
| Salario | 0.50 | 1.00 | 0.70 |
| Experiencia | 0.85 | 0.70 | 1.00 |

---

Interpretación

```text
Edad y Experiencia

r = 0.85

Relación positiva fuerte.
```

---

# Heatmap de Correlación

Visualización típica en análisis de datos.

---

```text
          Edad  Salario  Exp

Edad      ████  ███     ████

Salario   ███   ████    ███

Exp       ████  ███     ████
```

---

Los colores indican la fuerza de la relación.

---

# Ejemplo de Negocio

## Banco

Variables:

```text
Edad
Saldo
Cantidad de productos
```

---

Objetivo:

```text
Identificar relaciones importantes.
```

---

Resultado:

```text
Saldo vs Productos

r = 0.72
```

Interpretación:

```text
Los clientes con mayores saldos
suelen tener más productos contratados.
```

---

# Ejemplo en Riesgo Operacional

Variables:

```text
Complejidad del caso
Tiempo de resolución
```

---

Resultado:

```text
r = 0.81
```

---

Interpretación:

```text
Existe una fuerte relación positiva.
```

A mayor complejidad:

```text
Mayor tiempo de atención.
```

---

# Correlaciones Engañosas

Ejemplo:

```text
Consumo de café
Productividad
```

---

Resultado:

```text
r = 0.60
```

---

Pregunta correcta:

```text
¿El café genera productividad?
```

Tal vez no.

Podrían existir variables ocultas:

- Experiencia.
- Puesto.
- Horas trabajadas.

---

# Significancia Estadística de una Correlación

También es posible calcular un p-value.

---

Ejemplo

```text
r = 0.40

p = 0.001
```

---

Interpretación:

```text
Existe evidencia estadística
de una relación.
```

---

Otro ejemplo

```text
r = 0.40

p = 0.40
```

---

Interpretación:

```text
La relación podría ser producto del azar.
```

---

# En Python (Pandas)

## Correlación Simple

```python
df["Edad"].corr(df["Salario"])
```

---

Resultado:

```python
0.73
```

---

Interpretación:

```text
Relación positiva fuerte.
```

---

# Matriz de Correlación

```python
df.corr()
```

---

Resultado:

```text
Correlación entre todas las variables numéricas.
```

---

# Heatmap con Seaborn

```python
import seaborn as sns

corr = df.corr()

sns.heatmap(
    corr,
    annot=True,
    cmap="coolwarm"
)
```

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

# Relación con EDA

Durante el análisis exploratorio debes identificar:

```text
Variables relacionadas
```

porque pueden:

- Explicar comportamientos.
- Detectar redundancias.
- Ayudar a construir modelos predictivos.
- Descubrir patrones ocultos.

---

# Preguntas que Responde

- ¿Dos variables están relacionadas?
- ¿La relación es positiva o negativa?
- ¿Qué tan fuerte es?
- ¿Vale la pena investigar más?
- ¿Existe evidencia estadística de asociación?

---

# Cheat Sheet Rápido

| Valor r | Interpretación |
|----------|---------------|
| +1 | Positiva perfecta |
| +0.8 | Positiva muy fuerte |
| +0.5 | Positiva moderada |
| 0 | Sin relación lineal |
| -0.5 | Negativa moderada |
| -0.8 | Negativa fuerte |
| -1 | Negativa perfecta |

---

# Diferencias Clave

| Concepto | Significado |
|-----------|-----------|
| Correlación | Asociación |
| Causalidad | Relación causa-efecto |
| Pearson | Relación lineal |
| Spearman | Relación monotónica |
| Scatter Plot | Visualizar relación |
| Heatmap | Múltiples correlaciones |
| p-value | Evidencia estadística |

---

# Regla para Data Analytics

Cuando recibas un dataset:

```python
df.corr()
```

Luego:

```python
sns.heatmap(...)
```

Y finalmente:

```python
sns.scatterplot(...)
```

Pregúntate siempre:

✅ ¿Existe relación?

✅ ¿Qué tan fuerte es?

✅ ¿Es positiva o negativa?

✅ ¿Tiene sentido para el negocio?

✅ ¿Podría existir una causa oculta?

✅ ¿Estoy confundiendo correlación con causalidad?

Porque encontrar relaciones entre variables es uno de los principales objetivos del análisis de datos, pero interpretarlas correctamente es lo que diferencia a un verdadero analista de alguien que solo ejecuta código.
