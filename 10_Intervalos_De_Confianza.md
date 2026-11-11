# Intervalos de Confianza

## Objetivo

Un intervalo de confianza permite estimar un valor desconocido de una población utilizando una muestra.

En lugar de decir:

```text
La media poblacional es exactamente 500
```

decimos:

```text
La media poblacional probablemente está
entre 480 y 520
```

---

# El Problema

Normalmente no conocemos la población completa.

Por ejemplo:

```text
Clientes del banco: 1,000,000
```

Analizamos una muestra:

```text
2,000 clientes
```

y obtenemos:

```text
Edad promedio = 35 años
```

---

Pregunta:

```text
¿La edad promedio de TODA la población
también es exactamente 35?
```

Probablemente no.

Por eso construimos un intervalo de confianza.

---

# Definición

Un intervalo de confianza es un rango de valores dentro del cual esperamos encontrar el parámetro poblacional con un determinado nivel de confianza.

---

# Componentes

Un intervalo tiene tres elementos:

## Estadístico

Valor calculado sobre la muestra.

Ejemplo:

```text
Media muestral = 35
```

---

## Margen de Error

La incertidumbre asociada a la estimación.

Ejemplo:

```text
± 2 años
```

---

## Nivel de Confianza

Qué tan confiados estamos en la estimación.

Ejemplo:

```text
95%
```

---

# Estructura General

```text
Estimación ± Margen de Error
```

---

Ejemplo

```text
35 ± 2
```

Resultado:

```text
[33, 37]
```

---

Interpretación:

```text
Estimamos que la media real
está entre 33 y 37 años.
```

---

# Ejemplo Completo

Supongamos:

```text
Muestra = 1,000 clientes

Edad promedio = 35 años

Margen de error = 2 años
```

---

Intervalo:

```text
33 a 37 años
```

---

Visualización:

```text
33 -------- 35 -------- 37
|            ▲           |
|         Estimación     |
Intervalo de Confianza
```

---

# ¿Qué Significa un 95% de Confianza?

Esta es una de las partes más mal interpretadas de la estadística.

Mucha gente cree que significa:

```text
Hay 95% de probabilidad
de que la media esté ahí.
```

Eso NO es correcto.

---

La interpretación correcta es:

```text
Si tomáramos muchas muestras
y construyéramos muchos intervalos,
aproximadamente el 95% contendrían
al verdadero parámetro poblacional.
```

---

# Ejemplo Visual

Imagina que repites el estudio 100 veces.

```text
Muestra 1  → ✅

Muestra 2  → ✅

Muestra 3  → ✅

...

Muestra 96 → ✅

Muestra 97 → ✅

Muestra 98 → ❌

Muestra 99 → ❌

Muestra100 → ❌
```

---

Resultado:

```text
95 intervalos contienen
el valor real.

5 intervalos no.
```

---

# Niveles de Confianza Comunes

| Nivel | Interpretación |
|---------|---------|
| 90% | Menor precisión |
| 95% | Más utilizado |
| 99% | Mayor confianza |

---

# Comparación Visual

## 90%

```text
-----|=====|-----
```

Intervalo más estrecho.

---

## 95%

```text
----|=======|----
```

Más amplio.

---

## 99%

```text
---|==========|---
```

Más amplio aún.

---

# Regla Práctica

Mayor confianza:

```text
Más ancho el intervalo
```

---

Menor confianza:

```text
Más estrecho el intervalo
```

---

# Margen de Error

Representa cuánto puede variar nuestra estimación.

---

Ejemplo

Encuesta electoral:

```text
Candidato A

40%

± 3%
```

---

Intervalo:

```text
37% - 43%
```

---

Interpretación:

```text
El apoyo real podría
estar dentro de ese rango.
```

---

# Factores que Afectan el Intervalo

## Tamaño de Muestra

Más muestra:

```text
Mayor precisión
```

---

Intervalo:

```text
Más pequeño
```

---

## Menos Muestra

```text
Menor precisión
```

---

Intervalo:

```text
Más grande
```

---

# Ejemplo

## Muestra pequeña

```text
50 personas
```

```text
35 ± 8
```

Intervalo:

```text
27 - 43
```

---

## Muestra grande

```text
5,000 personas
```

```text
35 ± 1
```

Intervalo:

```text
34 - 36
```

---

# Relación con la Desviación Estándar

Si los datos están muy dispersos:

```text
Mayor incertidumbre
```

---

Resultado:

```text
Intervalo más amplio
```

---

Si los datos son homogéneos:

```text
Menor incertidumbre
```

---

Resultado:

```text
Intervalo más estrecho
```

---

# Fórmula Conceptual

(No es necesario memorizarla al inicio)

```text
Intervalo =
Media ± Error Estándar
```

---

Forma completa:

```text
Media ± Z × (σ / √n)
```

Donde:

```text
Z = nivel de confianza

σ = desviación estándar

n = tamaño de muestra
```

---

# Intuición de la Fórmula

Si aumenta:

```text
n
```

entonces:

```text
σ / √n
```

disminuye.

Resultado:

```text
Intervalos más precisos
```

---

# Ejemplo de Negocio

## Tiempo de Resolución

Muestra:

```text
500 incidentes
```

---

Promedio:

```text
8 días
```

---

IC 95%:

```text
7.5 - 8.5 días
```

---

Interpretación:

```text
Estimamos que el promedio real
de resolución está entre
7.5 y 8.5 días.
```

---

# Ejemplo Bancario

Muestra:

```text
1,000 clientes
```

---

Saldo promedio:

```text
Q 15,000
```

---

IC 95%

```text
Q 14,200 - Q 15,800
```

---

Interpretación:

```text
El saldo promedio real
probablemente se encuentra
entre esos valores.
```

---

# Relación con Distribución Normal

La distribución normal permite construir intervalos de confianza.

Recordatorio:

```text
68%  → ±1σ

95%  → ±2σ

99.7% → ±3σ
```

---

Por eso ambos temas están estrechamente relacionados.

---

# Error Estándar

## Definición

Mide la variabilidad de la media muestral.

No debe confundirse con la desviación estándar.

---

## Diferencia

### Desviación Estándar

```text
Variabilidad de los datos.
```

---

### Error Estándar

```text
Variabilidad de la estimación.
```

---

# En Python (SciPy)

## Intervalo de Confianza para la Media

```python
import scipy.stats as stats

stats.t.interval(
    confidence=0.95,
    df=len(datos)-1,
    loc=np.mean(datos),
    scale=stats.sem(datos)
)
```

---

# Con Pandas

Media:

```python
df["Salario"].mean()
```

---

Desviación:

```python
df["Salario"].std()
```

---

Cantidad de datos:

```python
df["Salario"].count()
```

---

# Ejemplo Simplificado

```python
media = df["Salario"].mean()

desv = df["Salario"].std()

n = df["Salario"].count()
```

---

Error estándar:

```python
desv / (n ** 0.5)
```

---

# Aplicación en Machine Learning

Los intervalos permiten responder:

```text
¿Qué tan confiable es una métrica?
```

---

Ejemplo

Accuracy:

```text
85%
```

---

IC 95%

```text
82% - 88%
```

---

Interpretación:

```text
La precisión real del modelo
probablemente se encuentra
en ese rango.
```

---

# Relación con los Próximos Temas

```text
Muestreo
      ↓
Distribución Normal
      ↓
Intervalos de Confianza
      ↓
Hipótesis
      ↓
P-Value
```

Los intervalos de confianza son el puente entre la estimación y la toma de decisiones estadísticas.

---

# Preguntas que Responde

- ¿Cuál es el rango probable del parámetro real?
- ¿Qué tan confiable es la estimación?
- ¿Mi muestra es suficientemente precisa?
- ¿Qué tan grande es la incertidumbre?
- ¿Necesito más datos?

---

# Cheat Sheet Rápido

| Concepto | Significado |
|-----------|-----------|
| Intervalo de Confianza | Rango probable del parámetro |
| Nivel de Confianza | Grado de certeza (90%,95%,99%) |
| Margen de Error | Amplitud de incertidumbre |
| Error Estándar | Variabilidad de la estimación |
| Mayor muestra | Intervalo más pequeño |
| Menor muestra | Intervalo más grande |
| Mayor dispersión | Intervalo más grande |
| Menor dispersión | Intervalo más pequeño |

---

# Regla para Data Analytics

Cuando veas una métrica como:

```text
Promedio = 8.2
```

pregunta inmediatamente:

```text
¿Con qué nivel de confianza?

¿Cuál es el margen de error?

¿Cuál es el intervalo de confianza?
```

Un promedio aislado rara vez cuenta toda la historia. El intervalo de confianza te muestra cuánta incertidumbre existe detrás de la cifra y qué tan confiable es para tomar decisiones.
