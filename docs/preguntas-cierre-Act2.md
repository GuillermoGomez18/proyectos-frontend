1. ¿Que problema resuelve la interfaz Gif dentro del proyecto?
Basicamente pone las reglas de que datos debe llevar cada objeto. Asi TypeScript nos avisa si nos falta algo o pusimos un dato mal antes de correr el programa.

2. ¿Que diferencia existe entre una interfaz y un objeto literal?
La interfaz es nomas el molde que dice como debe ser el dato, y el objeto literal ya es el dato real con la informacion guardada.

3. ¿Que significa Gif[] y que error evita en el arreglo local?
Quiere decir que en ese arreglo puro objeto que tenga la forma de Gif puede entrar. Nos salva de meter basura o datos que nada que ver por accidente.

4. ¿Por que username y description pueden declarse como propiedades opcionales?
Porque le ponemos el signo de interrogacion ? al declararlas. Con eso TypeScript ya sabe que no hay problema si un gif no trae esa info y no nos avienta error.

5. ¿En que situacion utilizarias let en lugar de const dentro de esta actividad?
Usaria let nomas cuando sepa que ese valor va a cambiar o lo voy a reescribir por completo mas adelante en el codigo.

6. ¿Que reciben y que devuelven normalizeText, searchGifs y createGifCard?
normalizeText: le pasas un string y te regresa otro string.

searchGifs: le pasas el arreglo de Gif[] y un string, y te regresa otro arreglo de Gif[].

createGifCard: le pasas un objeto Gif y te regresa un string que viene siendo el HTML.

7. ¿Que diferencia existe entre forEach, filter, map y find?
forEach: hace algo por cada elemento pero no te crea un arreglo nuevo.

filter: te hace un arreglo nuevo pero nomas con los que pasaron la condicion.

map: te arma un arreglo nuevo transformando cada dato.

find: busca y te regresa nomas el primer elemento que cumpla con lo que pides.

8. ¿Por que find puede devolver undefined y como se controlo ese resultado?
Te regresa undefined si de plano no encuentra nada. Lo controle usando ?. para que no truene al buscar la propiedad y ?? para ponerle un texto por default si viene vacio.

9. ¿Que es un callback? Identifica dos callbacks presentes en tu solucion.
Es una funcion que le pasamos a otra funcion para que la ejecute. En mi codigo use una en el filter (gif) => matchesQuery(gif, query) y otra en el map (tag) => '#${tag}'.

10. ¿Que ventaja ofrecen las template strings al construir las tarjetas?
Hacen un parote porque te dejan meter variables directo en el HTML usando los acentos graves y poniendo la variable entre ${...}.

11. ¿Para que se utilizo la destructuracion y el valor predeterminado de username?
La destructuracion es para sacar las variables del objeto directo, y el valor predeterminado es para que si el gif no trae autor, no salga un feo undefined en la pantalla.

12. ¿Por que querySelector puede devolver null y como se validaron los elementos?
Porque si escribimos mal el ID o no existe en el HTML te regresa un null. Le meti un if para que aviente un error si falta algo y asi TypeScript ya confia en que todo esta bien.

13. ¿Que funcion cumple preventDefault en el envio del formulario?
Sirve para que la pagina no se recargue toda cada vez que le damos al boton de buscar en el formulario.

14. ¿Como responde la aplicacion cuando la busqueda no obtiene coincidencias?
Como los resultados son cero, la funcion renderGifs pone un mensaje en la pantalla diciendo que no hay nada y ahi corta el rollo con un return.

15. ¿Que cambiara cuando el arreglo local sea sustituido por datos de Giphy API?
Que ya no vamos a tener los datos quemados en nuestro codigo sino que los vamos a jalar de internet, asi que a fuerzas vamos a tener que checar que vengan bien antes de pintarlos en el HTML.

16. ¿Que error o dificultad encontraste y como comprobaste que quedo resuelto?
Tuve un problema porque me marcaba unas lineas rojas diciendo que mis variables status y gallery podian ser null. Lo resolvi poniendo un if para validar que los elementos del DOM si existieran antes de usarlos, y asi ya me dejo compilar. Tambien batalle poquito para meter la descripcion extra del desafio pero quedo listo modificando la interfaz y la funcion de busqueda.