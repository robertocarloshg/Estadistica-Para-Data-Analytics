# Muestreo

## Objetivo

El muestreo es el proceso de seleccionar una parte de una población para estudiar sus características y realizar inferencias sobre el conjunto completo.

Responde preguntas como:

- ¿Necesito analizar toda la población?
- ¿Cuántas observaciones debo estudiar?
- ¿Mi muestra representa correctamente a la población?
- ¿Puedo generalizar los resultados obtenidos?

---

# ¿Por qué existe el Muestreo?

En muchos escenarios analizar toda la población es imposible o demasiado costoso.

Ejemplos:

### Banco

```text
Clientes totales: 2,500,000
```

Analizar cada cliente puede ser muy costoso.

---

### Universidad

```text
Estudiantes: 50,000
```

No es práctico entrevistar a todos.

---

### Manufactura

```text
Producción diaria: 100,000 piezas
```

No es viable inspeccionar cada una.

---

Por ello se selecciona una muestra.

---

# Conceptos Fundamentales

## Población

Conjunto completo de elementos de interés.

Ejemplo:

```text
Todos los clientes del banco.
```

---

## Muestra

Subconjunto de la población utilizado para el análisis.

Ejemplo:

```text
5,000 clientes seleccionados.
```

---

## Individuo

Elemento particular de la población.

Ejemplo:

```text
Cliente #25487
```

---

## Parámetro

Valor real de la población.

Ejemplos:

```text
Media poblacional
Proporción poblacional
Varianza poblacional
```

Normalmente es desconocido.

---

## Estadístico

Valor calculado a partir de una muestra.

Ejemplos:

```text
Media muestral
Varianza muestral
Desviación estándar muestral
```

Se utiliza para estimar parámetros.

---

# Visualización General

```text
┌───────────────────────────┐
│         POBLACIÓN         │
│      100,000 clientes     │
└─────────────┬─────────────┘
              │
              ▼
┌───────────────────────────┐
│         MUESTRA           │
│       2,000 clientes      │
└─────────────┬─────────────┘
              │
              ▼
┌───────────────────────────┐
│         ANÁLISIS          │
└─────────────┬─────────────┘
              │
              ▼
┌───────────────────────────┐
│     INFERENCIAS SOBRE     │
│       LA POBLACIÓN        │
└───────────────────────────┘
```

---

# Error de Muestreo

Existe porque la muestra nunca será exactamente igual a la población.

Ejemplo:

```text
Edad promedio real:
35 años
```

Muestra:

```text
34.7 años
```

---

Diferencia:

```text
0.3 años
```

Ese es un error de muestreo.

---

# Muestra Representativa

Una muestra debe reflejar las características de la población.

---

## Buena muestra

Población:

```text
60% mujeres
40% hombres
```

Muestra:

```text
58% mujeres
42% hombres
```

Representativa.

---

## Mala muestra

Población:

```text
60% mujeres
40% hombres
```

Muestra:

```text
95% mujeres
5% hombres
```

Sesgada.

---

# Tipos de Muestreo

Existen dos grandes categorías:

```text
Probabilístico
No probabilístico
```

---

# Muestreo Probabilístico

Todos los elementos tienen una probabilidad conocida de ser seleccionados.

---

## Muestreo Aleatorio Simple

Todos tienen la misma probabilidad.

---

### Ejemplo

Población:

```text
[A][B][C][D][E][F][G][H]
```

Muestra:

```text
[B][D][F]
```

Seleccionados aleatoriamente.

---

### Ventajas

✅ Fácil de entender.

✅ Reduce sesgos.

---

### Desventajas

❌ Puede requerir listado completo de la población.

---

# Muestreo Sistemático

Se selecciona cada k-ésimo elemento.

---

### Ejemplo

Lista:

```text
1 2 3 4 5 6 7 8 9 10
```

Seleccionando cada 3 elementos:

```text
1 4 7 10
```

---

### Uso común

```text
Control de calidad.
```

---

# Muestreo Estratificado

La población se divide en grupos homogéneos.

Luego se toma una muestra de cada grupo.

---

### Ejemplo

Empresa:

```text
60% Operaciones

25% Tecnología

15% Finanzas
```

---

Muestra:

```text
60% Operaciones

25% Tecnología

15% Finanzas
```

---

### Ventajas

✅ Alta representatividad.

✅ Muy utilizado en encuestas.

---

# Muestreo por Conglomerados

Se divide la población en grupos naturales.

Luego se seleccionan grupos completos.

---

### Ejemplo

Universidad:

```text
Edificio A
Edificio B
Edificio C
Edificio D
```

Se analizan únicamente:

```text
Edificio B
Edificio D
```

---

### Ventaja

✅ Menor costo operativo.

---

# Muestreo No Probabilístico

La selección depende del criterio del investigador.

---

## Muestreo por Conveniencia

Se selecciona lo que está disponible.

---

### Ejemplo

Encuestar únicamente:

```text
Personas que pasan frente a ti.
```

---

### Riesgo

```text
Alta probabilidad de sesgo.
```

---

## Muestreo por Juicio

El investigador decide quién participa.

---

### Ejemplo

Seleccionar únicamente:

```text
Clientes VIP.
```

---

# Sesgos de Muestreo

## Definición

Errores sistemáticos que hacen que la muestra no represente correctamente a la población.

---

# Sesgo de Selección

Ejemplo:

```text
Encuesta online sobre uso de internet.
```

Problema:

```text
Excluye a quienes no usan internet.
```

---

# Sesgo de Supervivencia

Solo observamos casos exitosos.

---

Ejemplo

Analizar:

```text
Empresas que siguen activas.
```

Ignorando:

```text
Empresas que quebraron.
```

---

# Sesgo de Respuesta

Las personas responden de forma distinta a la realidad.

---

Ejemplo

Pregunta:

```text
¿Hace ejercicio diariamente?
```

Muchos responderán:

```text
Sí
```

aunque no sea cierto.

---

# Tamaño de Muestra

## Pregunta frecuente

¿Cuántos registros necesito?

---

No existe una regla universal.

Depende de:

- Tamaño de población.
- Nivel de confianza.
- Margen de error.
- Variabilidad.

---

# Regla Práctica para Data Analytics

Si tienes:

```text
100,000 registros
```

analizar:

```text
5,000 o 10,000
```

suele ser suficiente para muchas tareas exploratorias.

---

# Muestreo en Ciencia de Datos

Situación:

```text
50 millones de registros
```

---

Problema:

```text
Tiempo
Memoria
Costo computacional
```

---

Solución:

```python
df.sample(100000)
```

---

Analizas una muestra representativa.

---

# Muestreo en Machine Learning

Muchas veces se divide el dataset:

```text
Entrenamiento
Validación
Prueba
```

---

Ejemplo

```text
70% Training

15% Validation

15% Testing
```

---

Visualización

```text
Dataset Completo

┌───────────────┐
│   100,000     │
└───────┬───────┘
        ▼

┌───────────────┐
│ 70,000 Train  │
├───────────────┤
│ 15,000 Valid  │
├───────────────┤
│ 15,000 Test   │
└───────────────┘
```

---

# En Python con Pandas

## Muestreo Aleatorio

```python
df.sample(100)
```

Obtiene:

```text
100 filas aleatorias.
```

---

## Muestreo Porcentaje

```python
df.sample(frac=0.10)
```

Obtiene:

```text
10% de los registros.
```

---

## Reproducibilidad

```python
df.sample(
    n=100,
    random_state=42
)
```

Genera siempre la misma muestra.

---

# Ejemplo de Negocio

## Banco

Población:

```text
500,000 clientes
```

---

Muestra:

```text
5,000 clientes
```

---

Análisis:

```text
Edad promedio
Saldo promedio
Morosidad
Satisfacción
```

---

Resultado:

```text
Se infieren características de toda la cartera.
```

---

# Relación con Temas Anteriores

```text
Población
     ↓
Muestra
     ↓
Media
Mediana
Moda
     ↓
Distribución
     ↓
Intervalos de Confianza
     ↓
Pruebas de Hipótesis
```

Sin una muestra adecuada, toda la inferencia estadística pierde validez.

---

# Preguntas que Responde

- ¿Cuántos casos debo analizar?
- ¿La muestra es representativa?
- ¿Puedo generalizar mis resultados?
- ¿Existe sesgo?
- ¿Qué tan confiables son mis conclusiones?

---

# Cheat Sheet Rápido

| Concepto | Significado |
|-----------|-----------|
| Población | Todos los elementos |
| Muestra | Subconjunto de la población |
| Individuo | Unidad observada |
| Parámetro | Valor real de la población |
| Estadístico | Valor calculado en la muestra |
| Aleatorio Simple | Todos tienen igual probabilidad |
| Sistemático | Cada k elementos |
| Estratificado | Por grupos representativos |
| Conglomerados | Por grupos completos |
| Sesgo | Distorsión de representatividad |

---

# Regla para Data Analytics

Antes de analizar cualquier dataset, pregúntate:

✅ ¿Es toda la población o una muestra?

✅ ¿Cómo fue seleccionada la muestra?

✅ ¿Puede existir sesgo?

✅ ¿Representa correctamente la realidad?

✅ ¿Puedo extrapolar los resultados?

Muchas decisiones equivocadas en análisis de datos no provienen de malos modelos, sino de muestras incorrectas. Un modelo sofisticado sobre una mala muestra produce conclusiones incorrectas con gran precisión.
