# Varianza y Desviación Estándar

## Objetivo

Medir qué tan dispersos están los datos.

## Ejemplo A

```text
10
11
9
10
10
```

Baja dispersión.

## Ejemplo B

```text
1
5
18
27
35
```

Alta dispersión.

## Visualización

```text
Baja Dispersión

8  9 10 11 12
   ●●●●●

Alta Dispersión

0     10     20     30     40
●         ●      ●      ●
```

## Varianza

Mide el alejamiento respecto a la media.

### Python

```python
df["Salario"].var()
```

## Desviación Estándar

Raíz cuadrada de la varianza.

### Python

```python
df["Salario"].std()
```

## Interpretación

- Baja → datos homogéneos.
- Alta → datos dispersos.

## Ejemplo de negocio

Salarios muy dispersos:

```text
2000
3000
5000
12000
25000
```

La empresa tiene grandes diferencias salariales.
