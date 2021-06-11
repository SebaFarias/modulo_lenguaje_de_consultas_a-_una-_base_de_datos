# Módulo 2 - SQL día 4 semana 7

## Captura
![Captura de pantalla](./Captura.png)
## Ejercicio 1

### Determinar nombre, apellido, cargo y departamento al cual pertenece el empleado con el mayor sueldo
    select nombre, apellidoP, cargo, departamento from Empleado order by sueldo desc limit 0,1;
### Determinar nombre, apellido, cargo y departamento al cual pertenece el empleado con el menor sueldo
    select nombre, apellidoP, cargo, departamento from Empleado order by sueldo asc limit 0,1;  
### Determinar cuantos empleados hay por departamento dentro de la   empresa
    select departamento, count(nombre) as empleados from Empleado group by departamento;
### Determinar cuanto es el gasto total mensual en sueldos dentro de la empresa.
    select sum(sueldo) as gastoMensual from Empleado;
### Agrupar por editorial y determinar cuántos libros pertenecen a cada una.
    select editorial, SUM(ejemplares) as ejemplares from Libro group by editorial;
### Determinar la cantidad de libros en existencia dentro de la biblioteca(ejemplares).
    select SUM(ejemplares) as TotalLibros from Libro;
## Ejercicio 2
