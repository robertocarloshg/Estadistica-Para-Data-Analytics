# Cuartiles y Percentiles

## Objetivo

Los cuartiles y percentiles permiten conocer la posición relativa de un dato dentro de una distribución.

Responden preguntas como:

- ¿Mi salario está por encima del 75% de los empleados?
- ¿Este estudiante está dentro del 10% con mejores notas?
- ¿Qué valor separa al 25% inferior del resto?
- ¿Dónde se encuentra un cliente respecto a todos los demás?

---

# Conceptos Previos

## Datos Ordenados

Para calcular cuartiles o percentiles, los datos deben ordenarse de menor a mayor.

Ejemplo:

```text
10, 20, 30, 40, 50, 60, 70, 80, 90, 100
```

---

# Percentiles

## Definición

Un percentil divide los datos en 100 partes iguales.

Cada percentil indica el porcentaje de observaciones que se encuentran por debajo de un valor determinado.

---

## Interpretación

### Percentil 25 (P25)

```text
25% de los datos están por debajo
75% de los datos están por encima
```

---

### Percentil 50 (P50)

```text
50% de los datos están por debajo
50% de los datos están por encima
```

Este percentil corresponde a la mediana.

---

### Percentil 90 (P90)

```text
90% de los datos están por debajo
10% de los datos están por encima
```

---

## Ejemplo

Notas de estudiantes:

```text
40
50
55
60
65
70
75
80
85
95
```

Si un estudiante obtuvo:

```text
85 puntos
```

y corresponde al Percentil 90:

```text
Su nota es mejor que la del 90% de los estudiantes.
```

---

# Cuartiles

## Definición

Los cuartiles dividen los datos en 4 grupos iguales.

---

## Representación

```text
0%      25%      50%      75%      100%
|--------|--------|--------|--------|
         Q1       Q2       Q3
```

---

## Primer Cuartil (Q1)

```text
25% de los datos quedan debajo
75% de los datos quedan arriba
```

---

## Segundo Cuartil (Q2)

```text
Corresponde a la mediana

50% de los datos debajo
50% de los datos arriba
```

---

## Tercer Cuartil (Q3)

```text
75% de los datos debajo
25% de los datos arriba
```

---

# Ejemplo Completo

Datos:

```text
10, 20, 30, 40, 50, 60, 70, 80, 90, 100
```

---

## Q1

```text
25
```

---

## Q2

```text
55
