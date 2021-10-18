# Módulo 2 - SQL día 2, semana 7.

## Ejercicio 1: Crear las siguientes consultas.

#### 1.1 Determinar los datos de los libros con más de 100 ejemplares.
```SQL
SELECT idLibro, autor, nombreLibro, ejemplares FROM Libro WHERE  ejemplares > 100;
```

#### 1.2 Determinar el nombre, apellidoP, apellidoM y cargo de los empleados que tienen un sueldo sobre los $500.000 y que pertenecen al departamento Producción.
```SQL
SELECT nombre, apellidoP, apellidoM, cargo FROM Empleado WHERE sueldo > 500000 AND departamento = 'Producción';
```

#### 1.3 Determinar los datos de los libros que son de la editorial Planeta o Penguin Random House y de la categoría Novela.
```SQL
SELECT idLibro, autor, nombreLibro, editorial, edicion FROM Libro WHERE editorial IN('Planeta', 'Penguin Random House') AND categoria = 'Novela';
```

#### 1.4 Determinar los autores que tienen algunas de las siguientes categorias: educación o filosofía.
```SQL
SELECT autor, categoria FROM Libro WHERE categoria IN ('Educación', 'Filosofía');
```

#### 1.5 Determinar los empleados que pertenecen al departamento Recursos humanos.
```SQL
SELECT nombre, apellidoP, apellidoM, cargo FROM Empleado WHERE departamento = 'Recursos humanos';
```

## Ejercicio 2: Crear consultas usando `NOT IN`.
```SQL
SELECT nombre, apellidoP, apellidoM, departamento, cargo FROM Empleado WHERE departamento NOT IN ('Contabilidad', 'Marketing');

SELECT idLibro, autor, nombreLibro, editorial FROM Libro WHERE editorial NOT IN ('Planeta', 'Zig-Zag', 'Penguin Random House');
```

## Ejercicio 3: Crear consultas con `<>`.
```SQL
SELECT nombre, apellidoP, apellidoM, departamento, cargo FROM Empleado WHERE cargo <> 'Jefe de Area';

SELECT idLibro, autor, nombreLibro, añoPublicacion, categoria FROM Libro WHERE categoria <> 'Ficción';
```


## Ejercicio 4: Crear consultas con `BETWEEN`.
```SQL
SELECT idLibro, autor, nombreLibro, añoPublicacion FROM Libro WHERE añoPublicacion BETWEEN 1990 AND 1999;

SELECT nombre, apellidoP, apellidoM, departamento, cargo, sueldo FROM Empleado WHERE sueldo BETWEEN 500000 AND 1000000;
```

## Ejercicio 5: Crear consultas con `LIKE`.
```SQL
SELECT nombre, apellidoP, apellidoM FROM Empleado WHERE apellidoP LIKE 'F%';

SELECT nombreLibro, autor, categoria FROM Libro WHERE categoria LIKE 'Novela%';
```