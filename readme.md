### Práctica Modelado de datos e introducción a SQL
## Archivos entregados
* Diagrama entidad/relación en formato draw.io
* Script

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
He dejado en el código todas las subconsultas que me han ayudado a sacar la solución. He creado una vista para simplificar la consulta definitiva. Espero que la encuentres sin problemas donde dice **ESTA ES LA CONSULTA QUE SACA LAS COPIAS DISPONIBLES Y RESPONDE AL EJERCICIO 1** 😅

### Ejercicio 2: sacar los géneros favoritos de cada socio
Igual que antes, he dejado en el código las subconsultas que me han llevado a la solución. La definitiva está debajo de donde pone **ESTA ES LA CONSULTA FINAL PARA OBTENER EL NOMBRE DEL GÉNERO MÁS ESCOGIDO POR CADA SOCIO Y RESPONDER AL EJERCICIO 2**.

Por último, sí, en uno de los commits he escrito "archibo" en vez de "archivo"... ¡Se me ha ido el dedo!
