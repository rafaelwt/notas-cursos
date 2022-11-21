# Notas:
 - [flex-direction](#flex-direction) 
 - [min-width](#min-width) 
 - [Organizar las filas: flex-wrap](#flex-wrap)

## flex-direction
Por defecto, el valor de esta propiedad está establecido como row, que nos indica que el main axis irá en horizontal y de izquierda a derecha. Como contraposición, es importante conocer que el cross axis siempre será el eje perpendicular al definido anterior por lo que por defecto podemos decir que este eje irá en vertical y de arriba a abajo.
A parte del valor row, es posible orientar el main axis en vertical usando el valor column.


Por último, también es posible aplicar el valor reverse a ambas opciones, sin embargo hay que tener cuidado con esto ya que modificaría el orden visual pero no la estructura de nuestro HTML. Debido a esto, si es importante el orden en el que aparecen los elementos a nivel de lectura deberíamos evitar esta técnica ya que nos dará problemas de accesibilidad al acceder a la web con un lector de pantallas.
```
.container {
 	display: flex;
 	flex-direction: column | row | reverse;
}
```

## min-width
`La propiedad min-width se usa para determinar la anchura mínima de un elemento. Previene que la propiedad width pueda ser inferior que min-width`

## Organizar las filas: flex-wrap
si queremos que el contenido salte a la línea siguiente cuando no haya suficiente espacio disponible, podemos establecer el valor wrap que permite al contenedor crear múltiples líneas.
Por otro lado, cuando el main axis de nuestro contenedor es column debemos de tener en cuenta que la web crece en vertical de forma indefinida por lo que si no establecemos una altura fija a nuestro contenedor no veremos este comportamiento de wrapeo de columnas.


Y finalmente, al igual que la propiedad flex-direction, es posible establecer una valor de wrap-reverse. Aunque ya hemos visto que hay que tener cuidado con estras propiedades ya que podemos caer en grande problemas de accesibilidad.

```
.container {
	display: flex;
	gap: 1rem;
	flex-direction: row;
	flex-wrap: wrap;
}
```

### Establecer el espacio entre las filas: align-content y justify-content