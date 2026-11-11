# Media, Mediana y Moda

## Datos

```text
5, 8, 9, 10, 13
```

---

## Media

### Definición

Promedio de todos los valores.

### Fórmula

```text
Media = Σx / n
```

### Ejemplo

```text
(5 + 8 + 9 + 10 + 13) / 5

45 / 5

= 9
```

### Python

```python
df["Salario"].mean()
```

---

## Mediana

### Definición

Valor central de un conjunto ordenado.

### Ejemplo

```text
5, 8, 9, 10, 13
      ↑
      9
```

### Python

```python
df["Salario"].median()
```

---

## Moda

### Definición

Valor que más se repite.

### Ejemplo

```text
5, 8, 8, 9, 10, 13

Moda = 8
```

### Python

```python
df["Salario"].mode()
```

## Regla Rápida

| Medida | Responde |
|----------|----------|
| Media | Promedio |
| Mediana | Centro real |
| Moda | Valor más frecuente |

## Interpretación

✅ Media: útil cuando los datos son simétricos.

✅ Mediana: útil cuando existen valores extremos.

✅ Moda: útil para datos categóricos.
