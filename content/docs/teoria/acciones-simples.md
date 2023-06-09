# Acciones Simples

Son una recopilación de **funciones** que se utilizan en los primeros algoritmos **sin una clasificación precisa**. Aclaro que en el material teórico no se explican detalladamente, sino que se empiezan a utilizar directamente. La información que compartiré a continuación está basada en las presentaciones de las clases prácticas, así como en algunos recursos adicionales que me he robado de por ahí.

Están advertidos 🙄...

## Antes de escribir pseudocódigo

¡Atención a todos los estudiantes!

Antes de sumergirse en la escritura de pseudocódigo, es importante considerar las herramientas adecuadas para esta tarea. Y aquí viene una advertencia importante: **¡no caigas en la tentación de usar el Block de Notas!**

<!-- agregar imagen notepad.gif -->

El Block de Notas es básico, ineficiente y propenso a errores de indentación. No querrás arruinar tus algoritmos debido a un simple descuido. Por eso, te recomiendo encarecidamente que descargues cualquier otro editor de código disponible.

Entre las opciones más populares y recomendadas, encontramos [**Visual Studio Code**](https://code.visualstudio.com/) (no confundir con Visual Studio). Este potente editor de código te brindará una experiencia de escritura cómoda y ordenada. Además, cuenta con una amplia gama de extensiones que pueden mejorar tu flujo de trabajo y hacer que la programación sea más placentera.

<!-- Agregar imagen vscodeuwu.png -->

Así que no lo dudes, deja atrás la vagancia y descarga un editor de código adecuado. ¡Te aseguro que notarás la diferencia y tus algoritmos te lo agradecerán! 😉

### Estructura de un Programa Básico

```
Accion Un_ejemplo es
    Ambiente
        // aquí se declaran variables/c, se definen funciones/p...
    Algoritmo
        // donde ocurre la magia...
fin accion
```

### Cuidado con la indentación

La «indentación» en criollo, es cuando nos referirnos a la **sangría** del código. Por ahora no es indispensable, pero si se recomienda usarla, de lo contrario muere un perrito.

No, en serio, indentá bien 🙅‍♂️, es un horror ver el código todo descuajeringado.

{{< tabs "uniqueid" >}}
{{< tab "Sin indentar 🤬" >}}

```
Para i := 1 a 10 hacer
Si i mod 2 = 0 entonces
Escribir(i)
Fin si
Fin Para
```

{{< /tab >}}
{{< tab "Mal indentado 💀" >}}

```
  Para i := 1 a 10 hacer
            Si i mod 2 = 0 entonces
 Escribir(i)
     Fin si
Fin Para
```

{{< /tab >}}
{{< tab "Bien indentado 😇" >}}

```
Para i := 1 a 10 hacer
    Si i mod 2 = 0 entonces
        Escribir(i)
    Fin si
Fin Para
```

Tengo la constumbre de usar 4 espacios, que es la configuaración por defecto en muchos editores de código, en lenguajes como python en impresindible que sea así.

{{< /tab >}}
{{< /tabs >}}

## Comentarios

Todo texto que se escriba después de // es un comentario, y no afecta en la ejecución del código.

```
// soy un comentario
no soy un comentario
```

Los programadores buscan constantemente la perfección, pero la mente humana puede ser olvidadiza. Documentar el código se vuelve invaluable, especialmente cuando otros lo revisan. Como portadores de estos conocimientos, debemos perseverar en esta tarea. No escatimes en comentarios, ya que son esenciales para la comprensión y comunicación.

## Salida de datos

Como un susurro de conocimiento, la palabra «escribir» transmite los resultados del programa al mundo exterior. Los datos, imbuidos de sentido y propósito, pueden ser plasmados por pantalla.

```
Escribir( <UN TEXTO> )

// debes reemplazar <UN TEXTO> con el texto o expresión que quieras.
```

Ejemplos:

```
Escribir(“hola mundooo!!!”)
Escribir(“lo siguiente es una variable: ”, var_1)
Escribir(“lo siguiente es un resultado: ”, var_1 + var_2)
```

## Entrada de datos

Similar a un ritual ancestral, el programador puede abrir las puertas de la interacción con el usuario. Creando así un vínculo entre el reino digital y el mundo tangible, una conexión que permite que los datos ingresados desde afuera se asignen a una variable ya definida.

```
Leer( <VARIABLE> )

// Se le asigna un valor ingresado por teclado a la variable que se nombró entre <>.
```

Ejemplos:

```
Leer(a)
Leer(primer-nombre)
Leer(una_variable, otra_variable, ...)
```

{{< hint info >}}
**🔥 Importante!**  
Siempre antes de ocupar un `Leer()` es recomendable ocupar un `Escribir()` con un mensaje detallando qué queremos que el usuario ingrese por pantalla.

```
Escribir(“Ingrese la fecha de forma de Dia, Mes y Año: ”)
Leer(Dia, Mes, Anio)
```
{{< /hint >}}