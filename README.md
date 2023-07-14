# Estructura base proyecto calculadora con JavaScript

[Click aquí para ver proyecto base funcionnando](https://daferguerrero.github.io/proyecto-base-calculadora/)

A través de este este tutorial serás guiado paso a paso en la creación de una calculadora utilizando JavaScript. El repositorio contiene el código base HTML y CSS necesario para la interfaz de la calculadora, por lo cual está enfocado exclusivamente en explicar cómo funciona el código JavaScript en detalle. <br>

## Funciones Principales

#### `digitarEnDisplay(value)`
La finalidad de esta función es añadir el valor suministrado a través del display de la calculadora. Recibe un parámetro denominado `value` que representa el valor a agregar. Para obtener el elemento del documento HTML utilizando su identificador único (ID), se utiliza el método `document.getElementById("display")`, y posteriormente se actualiza el campo de `value` concatenando el nuevo valor del elemento.

>     function digitarEnDisplay(value) {
>     	document.getElementById("display").value += value;
>     }

#### `calcular()`
Cuando se presiona el botón de igual (=) en la calculadora, se activa la función `calcular()`. En primer lugar, se recupera el valor actual del display mediante el método `document.getElementById("display").value`. A continuación, se emplea la función `eval()` para evaluar la expresión matemática representada por dicho valor. El resultado obtenido se guarda en la variable `resultado` y se actualiza el display con el resultado calculado. . Por último, se agregar un evento de escucha al elemento HTML con el ID `calcular`, es decir, cuando se hace clic en ese elemento, se ejecutará la función `calcular()`.

>     function  calcular() {
>     const valorDisplay = document.getElementById("display").value;
>     const resultado =  eval(valorDisplay);
>     document.getElementById("display").value = resultado;
>     }

A continuación una explicación más detallada de cada parte de la línea de código de la función `calcular()`:
- `const valorDisplay`: Esta declaración crea una constante llamada 'valorDisplay' cuyo alcance puede ser global o local para el bloque en el que se declara. Es necesario inicializar la constante, es decir, se debe especificar su valor en la misma sentencia en la que se declara, lo que tiene sentido, dado que no se puede cambiar posteriormente.
- `calcular`: Es el nombre de la función. Esta función se ejecutará cuando se dispare el evento `"click"` en el elemento con el ID `"calcular"`.
<br>
- `document.getElementById("display")`: Esta parte busca un elemento HTML en el documento que tenga el ID `display`. `getElementById` es un método que pertenece al objeto document y se utiliza para obtener una referencia a un elemento específico en la página utilizando su ID.

#### `limpiarPantalla()`
Para borrar o eliminar el contenido de la pantalla o display de la calculadora se emplea la función `"limpiarDisplay()"`. Consiste en asignar una cadena vacía al campo `.value` del elemento que representa el display.

>     function limpiarDisplay() {
>     document.getElementById("display").value =  "";
>     }

Veamos los componentes de esta línea de código:
- `limpiarDisplay`: Es el nombre de una función que se ejecutará cuando se produzca el evento `"click"` en el elemento seleccionado. Esto proporciona la funcionalidad de limpiar cualquier contenido de la pantalla cuando se active el evento de `"click"` en el botón "`C`".

## Integración con HTML y CSS
Asegúrate de contar con un elemento HTML con el identificador "display" que representa la pantalla de la calculadora para poder utilizar estas funciones. Los archivos proporcionados en el repositorio contienen el código HTML y CSS correspondiente, los cuales puedes revisar.

Recuerda que puedes utilizar tu creatrividad y personalizar la interfaz y añadir más funcionalidades según tus propias necesidades.

¡Ya estás preparado/a para crear tu propia calculadora en JavaScript!. Sigue este tutorial y disfruta explorando el maravilloso mundo de la programación web.

## Contribución
¡Las contribuciones son bienvenidas! Si deseas contribuir a este proyecto, puedes seguir estos pasos:

1.  Haz un fork del repositorio.
2.  Crea una rama para tus cambios: `git checkout -b mi-rama`.
3.  Realiza los cambios deseados y realiza commits: `git commit -m "Descripción de los cambios"`.
4.  Envía tus cambios al repositorio remoto: `git push origin mi-rama`.
5.  Abre un pull request en GitHub y describe tus cambios en detalle.

## Licencia
Este proyecto se distribuye bajo la Licencia GPL (Licencia Pública General de GNU)

## Autor
Este proyecto fue creado por [David Fernando Guerrero Vanegas](https://github.com/daferguerrero).

## Contacto
Si tienes alguna pregunta o sugerencia relacionada con este proyecto, puedes contactarme a través de mi dirección de correo electrónico: [dafer.guerrero@gmail.com](dafer.guerrero@gmail.com).
