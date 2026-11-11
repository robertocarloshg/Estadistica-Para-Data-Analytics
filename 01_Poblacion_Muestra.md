# Población y Muestra

## Población

Conjunto completo de individuos u observaciones que son objeto de estudio.

## Muestra

Subconjunto representativo de la población utilizado para realizar el análisis.

## Ejemplo

```text
Empresa XYZ

Población:
5,000 empleados

Muestra:
500 empleados seleccionados
```

## Diagrama

```text
┌────────────────────────┐
│      POBLACIÓN         │
│    5,000 empleados     │
└──────────┬─────────────┘
           │
           ▼
┌────────────────────────┐
│       MUESTRA          │
│     500 empleados      │
└────────────────────────┘
```

## Interpretación

✅ Analizar la población completa suele ser costoso.

✅ La muestra permite estimar características de la población.

⚠️ Una muestra sesgada produce conclusiones incorrectas.

## Ejemplo de negocio

Quiero conocer la satisfacción de todos los clientes del banco.

- Población: 100,000 clientes.
- Muestra: 2,000 clientes encuestados.

## En Pandas

```python
df.shape
```

Permite conocer cuántos registros contiene la muestra.

## Preguntas que responde

- ¿A quién quiero estudiar?
- ¿Cuántos elementos analizaré?
