# Hipótesis y P-Value

## Objetivo

Las pruebas de hipótesis permiten determinar si una diferencia observada en una muestra es suficientemente importante como para concluir que existe un efecto real en la población.

Responden preguntas como:

- ¿Las ventas realmente aumentaron después de una campaña?
- ¿Un nuevo proceso es más eficiente que el anterior?
- ¿Dos grupos se comportan diferente?
- ¿La diferencia observada es real o producto del azar?

---

# Motivación

Supongamos que una empresa afirma:

```text
El tiempo promedio de resolución es 8 días.
```

Tomamos una muestra de casos y obtenemos:

```text
Promedio = 7.5 días.
```

---

Pregunta:

```text
¿La diferencia entre 8 y 7.5 es real?
```

o

```text
¿Puede explicarse simplemente por variación aleatoria?
```

---

Aquí entra la prueba de hipótesis.

---

# Conceptos Fundamentales

Una prueba de hipótesis siempre compara dos afirmaciones.

---

## Hipótesis Nula (H₀)

Representa la situación base.

Generalmente significa:

```text
No hay diferencia.
No hay efecto.
No hay cambio.
```

---

Ejemplo

```text
H₀: El tiempo promedio es 8 días.
```

---

## Hipótesis Alternativa (H₁)

Representa lo que queremos demostrar.

---

Ejemplo

```text
H₁: El tiempo promedio es diferente de 8 días.
```

---

# Ejemplo Visual

```text
Hipótesis Nula (H₀)

Promedio = 8 días


Hipótesis Alternativa (H₁)

Promedio ≠ 8 días
```

---

# Analogía del Juicio

La forma más sencilla de recordar las hipótesis.

---

## H₀

```text
El acusado es inocente.
```

Suposición inicial.

---

## H₁

```text
El acusado es culpable.
```

---

Mientras no exista suficiente evidencia:

```text
Se mantiene H₀.
```

No se demuestra inocencia.

Simplemente:

```text
No hay evidencia suficiente para rechazarla.
```

---

La estadística trabaja exactamente igual.

---

# Proceso de una Prueba de Hipótesis

```text
1. Formular H₀ y H₁
          ↓
2. Obtener muestra
          ↓
3. Calcular estadístico
          ↓
4. Calcular p-value
          ↓
5. Tomar decisión
```

---

# ¿Qué es el P-Value?

## Definición

El p-value mide qué tan compatibles son los datos observados con la hipótesis nula.

---

En términos simples:

```text
¿Qué tan extraño sería observar
estos resultados si H₀ fuera cierta?
```

---

# Interpretación Intuitiva

Si el p-value es muy pequeño:

```text
Lo observado sería muy raro
si H₀ fuera verdadera.
```

---

Implica:

```text
Hay evidencia contra H₀.
```

---

# Ejemplo

Supongamos:

```text
H₀:
Promedio = 8 días
```

---

Muestra:

```text
Promedio observado = 6 días
```

---

Resultado:

```text
p-value = 0.001
```

---

Interpretación:

```text
Existe apenas un 0.1%
de probabilidad de observar
una diferencia tan extrema
si H₀ fuera verdadera.
```

---

Conclusión:

```text
Rechazamos H₀.
```

---

# Nivel de Significancia (α)

Antes del análisis debemos definir un umbral.

Normalmente:

```text
α = 0.05
```

---

Eso equivale a:

```text
5%
```

---

# Regla de Decisión

## Caso 1

```text
p-value < 0.05
```

Resultado:

```text
Rechazar H₀
```

Existe evidencia estadística.

---

## Caso 2

```text
p-value ≥ 0.05
```

Resultado:

```text
No rechazar H₀
```

No existe evidencia suficiente.

---

# Cheat Visual

```text
               p-value

0 ----------------------------------- 1
|-----------|-------------------------|
      0.05

Rechazar H₀      No Rechazar H₀
```

---

# Ejemplo 1

## Ventas

Hipótesis:

```text
H₀: Ventas promedio = Q10,000

H₁: Ventas promedio ≠ Q10,000
```

---

Resultado:

```text
p-value = 0.03
```

---

Interpretación:

```text
0.03 < 0.05
```

---

Conclusión:

```text
Rechazamos H₀.
```

Hay evidencia de que el promedio es distinto de Q10,000.

---

# Ejemplo 2

## Satisfacción del Cliente

Hipótesis:

```text
H₀: Promedio = 80
```

---

Resultado:

```text
p-value = 0.42
```

---

Interpretación:

```text
0.42 > 0.05
```

---

Conclusión:

```text
No rechazamos H₀.
```

No hay evidencia suficiente de diferencia.

---

# Error Tipo I

## Definición

Rechazar una hipótesis verdadera.

---

Visualización:

```text
H₀ era verdadera

pero

la rechazamos
```

---

Ejemplo

El sistema realmente funciona.

Pero concluimos:

```text
Está defectuoso.
```

---

Probabilidad:

```text
α = 0.05
```

---

# Error Tipo II

## Definición

No rechazar una hipótesis falsa.

---

Visualización:

```text
H₀ era falsa

pero

la aceptamos
```

---

Ejemplo

El sistema tiene un problema.

Pero concluimos:

```text
Todo funciona bien.
```

---

# Tabla Resumen

| Realidad | Decisión | Resultado |
|-----------|-----------|-----------|
| H₀ verdadera | No rechazar | Correcto |
| H₀ verdadera | Rechazar | Error Tipo I |
| H₀ falsa | Rechazar | Correcto |
| H₀ falsa | No rechazar | Error Tipo II |

---

# Lo que el P-Value NO Significa

Muchos analistas lo interpretan incorrectamente.

---

Incorrecto:

```text
El p-value es la probabilidad
de que H₀ sea verdadera.
```

❌ Falso.

---

Incorrecto:

```text
p = 0.02

Entonces H₀ tiene un 2%
de probabilidad de ser cierta.
```

❌ Falso.

---

Interpretación correcta:

```text
Si H₀ fuera cierta,
la probabilidad de obtener
un resultado igual o más extremo
es 0.02.
```

✅ Correcto.

---

# Significancia Estadística vs Significancia Práctica

Este error es muy común en Data Analytics.

---

Ejemplo

Base de datos:

```text
10 millones de clientes
```

---

Resultado:

```text
Incremento promedio:

0.05%
```

---

P-value:

```text
0.000001
```

---

Estadísticamente:

```text
Significativo
```

---

Pero:

```text
¿Tiene impacto real?
```

Tal vez no.

---

Por eso siempre debemos preguntar:

```text
¿La diferencia es útil para el negocio?
```

y no solamente:

```text
¿Es significativa?
```

---

# Tipos de Pruebas de Hipótesis

No es necesario memorizar todas al inicio.

---

## T-Test

Comparar medias.

Ejemplo:

```text
Ventas antes y después.
```

---

## ANOVA

Comparar varias medias.

Ejemplo:

```text
3 sucursales distintas.
```

---

## Chi-Cuadrado

Comparar proporciones.

Ejemplo:

```text
Método de pago vs abandono.
```

---

# Ejemplo de Negocio

## Riesgo Operacional

Hipótesis:

```text
H₀:
Tiempo promedio = 8 días
```

---

Implementación de mejora:

```text
Nuevo flujo de aprobación
```

---

Resultado:

```text
Promedio actual = 6.5 días

p-value = 0.01
```

---

Conclusión:

```text
La reducción parece real
y no atribuible al azar.
```

---

# Relación con Intervalos de Confianza

Muchas veces ambas técnicas llevan a la misma conclusión.

---

Ejemplo

Diferencia promedio:

```text
2 días
```

---

IC 95%

```text
1.2 a 2.8 días
```

---

Como el cero no aparece:

```text
Existe evidencia de diferencia.
```

---

Normalmente:

```text
p-value < 0.05
```

---

# En Python (SciPy)

## T-Test

```python
from scipy.stats import ttest_1samp

estadistico, pvalue = ttest_1samp(
    datos,
    popmean=8
)

print(pvalue)
```

---

# Comparación de Dos Grupos

```python
from scipy.stats import ttest_ind

estadistico, pvalue = ttest_ind(
    grupo_a,
    grupo_b
)
```

---

# Regla Automática

```python
if pvalue < 0.05:
    print("Rechazar H0")
else:
    print("No rechazar H0")
```

---

# En Data Analytics

Cuando compares:

- Ventas
- Clientes
- Sucursales
- Procesos
- Campañas
- Modelos predictivos

pregúntate:

```text
¿La diferencia observada
es realmente significativa?
```

---

# Relación con los Temas Anteriores

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
      ↓
Toma de Decisiones
```

---

# Preguntas que Responde

- ¿Existe evidencia de una diferencia?
- ¿El cambio observado es real?
- ¿Puede ser producto del azar?
- ¿Debería modificar el proceso?
- ¿Los grupos se comportan igual?

---

# Cheat Sheet Rápido

| Concepto | Significado |
|-----------|-----------|
| H₀ | Hipótesis nula |
| H₁ | Hipótesis alternativa |
| α | Nivel de significancia (0.05) |
| p-value | Evidencia contra H₀ |
| p < 0.05 | Rechazar H₀ |
| p ≥ 0.05 | No rechazar H₀ |
| Error Tipo I | Falso positivo |
| Error Tipo II | Falso negativo |
| Significancia estadística | Diferencia detectada |
| Significancia práctica | Impacto real en negocio |

---

# Mentalidad de Analista

Cuando alguien te diga:

```text
Las ventas aumentaron.

Los tiempos mejoraron.

Los clientes están más satisfechos.
```

No aceptes la afirmación inmediatamente.

Pregunta:

```text
¿Cuál fue la muestra?

¿Cuál fue el p-value?

¿Cuál es el intervalo de confianza?

¿Cuál es el impacto para el negocio?
```

Ese es el punto donde dejas de ser alguien que genera reportes y comienzas a pensar como un analista de datos.
