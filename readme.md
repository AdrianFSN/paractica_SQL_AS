### Práctica Modelado de datos e introducción a SQL
## Archivos entregados
* Diagrama entidad/relación en formato draw.io
* Script
* Readme

## Diagrama
Lo he diseñado en siete tablas:
* Socio
* Dirección
* Película
* Director película
* Género
* Sinopsis
* Registro alquileres

### Algunas notas sobre las tablas
**Registro alquileres** es la pieza que permite conectar los socios con las películas.

**Socio** es la tabla desde la que se puede llegar a las direcciones postales de los socios.

**Película** es la tabla desde la que se puede acceder a las sinopsis, los directores y el género de cada título.

Pensé en hacer otra tabla para los títulos, pero creo que no era necesario complicar más el diagrama.

## El script
Después de crear las tablas, he ido comentando lo que hacía para no perderme. Espero que sea útil para vcer la lógica que he seguido para las dos consultas principales de la práctica.

### Ejercicio 1: sacar las copias disponibles de cada película
He dejado en el código todas las subconsultas que me han ayudado a sacar la solución. He creado una vista para simplificar la consulta definitiva. Espero que la encuentres sin problemas donde dice **ESTA ES LA CONSULTA QUE SACA LAS COPIAS DISPONIBLES Y RESPONDE AL EJERCICIO 1** 😅.

Lo que hago es calcular primero cuántas copias totales tengo de cada título.

Después, calculo cuantas copias de cada título están alquiladas, porque tienen fecha NULL.

Por último, resto a las copias totales las copias alquiladas.

### Ejercicio 2: sacar los géneros favoritos de cada socio
Igual que antes, he dejado en el código las subconsultas que me han llevado a la solución. La definitiva está debajo de donde pone **ESTA ES LA CONSULTA FINAL PARA OBTENER EL NOMBRE DEL GÉNERO MÁS ESCOGIDO POR CADA SOCIO Y RESPONDER AL EJERCICIO 2**.

En este caso, consulto primero todas las películas alquiladas por cada socio y los géneros que les corresponden.

Después, cuento las veces que se repite cada género entre todas las películas alquiladas por cada socio.

A continuación, saco el máximo de todas esas repeticiones que he calculado anteriormente para cada socio.

Resumo las consultas en vistas.

En la consulta final, uno y comparo ambas vistas. Filtro los resultados para que se muestren solo los que coindicen con el género por socio que tenía el valor máximo de puntuaciones.