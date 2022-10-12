# Repaso SQL

SQL es un lenguaje de programacion para base de datos. Su traduccion literal seria lenguaje estructurado de consultas (Structured Query Language)

SQL es un lenguaje insensible a mayusculas y minusculas, "select" == SELECT.

El sql las tablas tienen columnas tendran informacion de cierto **tipo**

Como buena practica los nombres de las tablas deben ser en **plural**

llave primaria: Con valor unico y no nulo.

CSV: Formato de archivo muy popular en loa negoios. A partir de XLS se pueden exportar datos en CSV y tambien importar."Valores separados por coma"

La sentencia **WHERE** es para filtrar informacion

```sql
SELECT <column>
FROM <table>;
WHERE <column> <condition>;
```

```sql
SELECT name, country, area
FROM cities
WHERE area < 1100
AND country = 'Japan';
```

### Ejemplo usando **OR**
```sql
SELECT name, country, area
FROM cities
WHERE area < 1100
OR country = 'Japan';
```

### Ejemplo ordenando los resultados en forma ascendente

```sql
SELECT name, country, area
FROM cities
ORDER BY area;
```
### Ejemplo con WHERE, OR y ORDER

```sql
SELECT name, country, area
FROM cities
WHERE area < 1100
OR country = 'Japan'
ORDER BY area;
```
### Ejemplo descendente

```sql
SELECT name, country, area
FROM cities
WHERE area < 1100
OR country = 'Japan'
ORDER BY area DESC;
```
>Nota: Distinto puede ser <> o !=

## Campos o columna calculados con AS (como)

```sql
SELECT name, population/area AS density
FROM cities
ORDER BY density DESC;
```

```sql
SELECT name, population/area AS density
FROM cities
ORDER BY density ASC;
```
## Contando elementos con COUNT

```sql
SELECT COUNT(name)
FROM cities
WHERE country = 'India';
```

## Limitar los resultados con **Limit**

```sql
SELECT name, population/area AS density
FROM cities
ORDER BY density DESC
LIMIT 2;
```


