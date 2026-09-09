# Preguntas de cierre EC1 F2 A3


## 1. ¿Que significa refactorizar una aplicacion?
Basicamente es darle una buena acomodada y limpiada al codigo por dentro para que quede mejor organizado, pero sin cambiar lo que hace la aplicacion por fuera ni romper nada de lo que ya funcionaba.

## 2. ¿Por que el proyecto se dividio en modulos?
Para no tener todo el codigo en un solo archivo. Asi cada parte tiene su propio trabajo (como los datos, la interfaz, las busquedas) y es mucho mas facil de mantener y leer despues.

## 3. ¿Cual es la responsabilidad de main.ts?
Viene siendo el jefe que coordina todo. Su chamba es inicializar la interfaz y conectar todos los modulos para que trabajen juntos, pero sin repetir el codigo que ya esta en las otras carpetas.

## 4. ¿Que diferencias existen entre una interfaz, un tipo union y una enumeracion?
- La interfaz es como el contrato que te dice que propiedades debe llevar un objeto.
- El tipo union es para limitar una variable a que solo acepte unos cuantos valores exactos (como las clasificaciones de edad).
- Y la enumeracion agrupa varios estados o valores que tienen relacion bajo un mismo nombre para no andar escribiendo el texto a cada rato.

## 5. ¿Para que se utiliza import type?
Se usa para decirle a TypeScript que vamos a usar ese archivo solo para checar los tipos, asi cuando se compila a JavaScript no se lleva codigo innecesario que solo hace bulto.

## 6. ¿Donde se aplicaron la desestructuracion, spread y rest?
- La desestructuracion la use en los componentes de la galeria y el detalle para sacar las propiedades directo del objeto y no escribir gif.algo a cada rato.
- El spread (...) lo use para meter las etiquetas a la busqueda y para copiar el arreglo de la coleccion.
- Y el rest lo use en el detalle para separar la etiqueta principal de las demas etiquetas secundarias en el arreglo.

## 7. ¿Por que searchGifs recibe la coleccion como parametro?
Porque ese modulo solo es un servicio de busqueda, entonces necesita que le pases los datos sobre los que va a buscar y filtrar.

## 8. ¿Por que findGifById puede devolver undefined?
Porque usamos la funcion find, y si da la casualidad de que buscas un ID que no existe, pues te va a regresar undefined. Al decirle esto a TypeScript, nos obliga a poner un if para validar que si encontro algo antes de pintar el detalle en pantalla.

## 9. ¿Que funcion cumple data-gif-id?
Sirve para guardarle el ID del gif directo en el boton del HTML, asi cuando el usuario le da clic a "Ver detalle", sabemos exactamente cual gif escogio.

## 10. ¿Que es la delegacion de eventos?
Es un truco para no poner un evento de clic a cada boton que se genera. Mejor le ponemos el evento al contenedor grande (la galeria) y desde ahi sabemos a cual boton en especifico se le dio el clic.

## 11. ¿Por que el estado Loading podria no observarse?
Porque estamos buscando en un arreglo local en la computadora, la busqueda es tan rapida que termina antes de que el navegador alcance a mostrar el mensaje de cargando.

## 12. ¿Que dificultad se presento durante la refactorizacion y como se resolvio?
Me salio un error con el Enum de RequestStatus porque la configuracion no me dejaba usarlo. Lo resolvi metiendome al archivo tsconfig.json y cambiando la propiedad erasableSyntaxOnly a false para que ya me dejara compilar bien. Un error que sabiamos que pasaria debido a la naturaleza de tsconfig.json, fuera de eso no tuve ningun problema
