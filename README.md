# Estructura base proyecto calculadora con JavaScript

[Click aquí para ver proyecto base funcionnando](https://daferguerrero.github.io/proyecto-base-calculadora/)

A tarvés de este este tutorial serás guiado paso a paso en la creación de una calculadora utilizando JavaScript. El repositorio contiene el código base HTML y CSS necesario para la interfaz de la calculadora, por lo cual está enfocado exclusivamente en explicar cómo funciona el código JavaScript en detalle. <br>

## Funciones Principales

#### `digitarEnDisplay(value)`
La finalidad de esta función es añadir el valor suministrado a través del display de la calculadora. Recibe un parámetro denominado `value` que representa el valor a agregar. Para obtener el elemento del documento HTML utilizando su identificador único (ID), se utiliza el método `document.getElementById("display")`, y posteriormente se actualiza el campo de `value` concatenando el nuevo valor del elemento.

>     function digitarEnDisplay(value) {
>     	document.getElementById("display").value += value;
>     }
<br>

#### `calcular()`
Cuando se presiona el botón de igual (=) en la calculadora, se activa la función `calcular()`. En primer lugar, se recupera el valor actual del display mediante el método `document.getElementById("display").value`. A continuación, se emplea la función `eval()` para evaluar la expresión matemática representada por dicho valor. El resultado obtenido se guarda en la variable `resultado` y se actualiza el display con el resultado calculado. . Por último, se agregar un evento de escucha al elemento HTML con el ID `calcular`, es decir, cuando se hace clic en ese elemento, se ejecutará la función `calcular()`.

>     function  calcular() {
>     const valorDisplay = document.getElementById("display").value;
>     const resultado =  eval(valorDisplay);
>     document.getElementById("display").value = resultado;
>     }
>     
>     document.getElementById("calcular").addEventListener("click", calcular);

A continuación una explicación más detallada de cada parte de la línea de código de la función `calcular()`:

- `document.getElementById("calcular")`: Esta parte busca un elemento HTML en el documento que tenga el ID `calcular`. `getElementById` es un método que pertenece al objeto document y se utiliza para obtener una referencia a un elemento específico en la página utilizando su ID.

- `.addEventListener("click", calcular)`: Después de obtener la referencia al elemento con el ID `"calcular"`, se llama al método `addEventListener` en ese elemento. Este método se utiliza para adjuntar un evento a un elemento HTML. En este caso, el evento que se adjunta es `"click"`, lo que significa que se activará cuando se haga clic en el elemento.

- `calcular`: Es el nombre de la función. Esta función se ejecutará cuando se dispare el evento `"click"` en el elemento con el ID `"calcular"`.
<br>

#### `limpiarPantalla()`
Para borrar o eliminar el contenido de la pantalla o display de la calculadora se emplea la función `"limpiarDisplay()"`. Consiste en asignar una cadena vacía al campo `.value` del elemento que representa el display.

>     function limpiarDisplay() {
>     document.getElementById("display").value =  "";
>     } 
>     
>     document.getElementById("btn-limpiar").addEventListener("click", limpiarDisplay);

`document.getElementById("btn-limpiar").addEventListener("click", limpiarDisplay);`<br>
Esta línea de código se utiliza para agregar un "event listener" o "escuchador de eventos" a un elemento del documento HTML. Veamos los componentes de esta línea de código:

- `document.getElementById("btn-limpiar")`: Se utiliza para seleccionar un elemento HTML con el atributo id `"btn-limpiar"`. El método `getElementById` busca y devuelve el elemento correspondiente en el documento.

- `.addEventListener("click", limpiarDisplay)`: Es un método que se aplica al elemento seleccionado en el paso anterior. Aquí se está agregando un `"eventlistener"` para el evento `"click"` al elemento.

- `limpiarDisplay`: Es el nombre de una función que se ejecutará cuando se produzca el evento `"click"` en el elemento seleccionado. Esto proporciona la funcionalidad de limpiar cualquier contenido de la pantalla cuando se active el evento de `"click"` en el botón "`C`".

 <br>

## Integración con HTML y CSS
Asegúrate de contar con un elemento HTML con el identificador "display" que representa la pantalla de la calculadora para poder utilizar estas funciones. Los archivos proporcionados en el repositorio contienen el código HTML y CSS correspondiente, los cuales puedes revisar.

Recuerda que puedes utilizar tu creatrividad y personalizar la interfaz y añadir más funcionalidades según tus propias necesidades.

¡Ya estás preparado/a para crear tu propia calculadora en JavaScript!. Sigue este tutorial y disfruta explorando el maravilloso mundo de la programación web.
