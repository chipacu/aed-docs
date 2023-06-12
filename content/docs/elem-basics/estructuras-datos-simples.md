---
title: Estructuras de Datos Simples
weight: 2
---

# Estructuras de Datos Simples

![recipe](/aed-docs/images/archiver.jpg)

A la hora de elaborar un programa, **es necesario utilizar datos**. Por ejemplo, si queremos calcular el área de un rectángulo, debemos almacenar en la memoria de la computadora los valores de la base y la altura para luego multiplicarlos y obtener el área.

Es importante recordar que hay una diferencia entre grabar los datos en la memoria y grabarlos en el disco duro. Cuando hablamos de grabar en memoria, nos referimos a almacenar los datos en la RAM. Para hacer esto, utilizamos dos elementos: variables y constantes. Estos nos permiten **guardar y manipular** los datos necesarios para realizar los cálculos en el programa.

{{< columns >}}
## Variables
Son elementos de almacenamiento de datos. Representan una dirección de memoria en donde se almacena un dato, y **su contenido puede variar** en el desarrollo del algoritmo.

<---> 

## Constantes
Al igual que una variable, representa una zona de memoria en la cual se almacena un dato. Sin embargo **su contenido no puede modificarse** durante la ejecución.

{{< /columns >}}

Antes de asignarle un valor, debemos definirlas de la siguiente manera:

{{< tabs "uniqueid" >}}
{{< tab "Variables" >}} ```a : Entero``` {{< /tab >}}
{{< tab "Constantes" >}} ```a = Entero``` {{< /tab >}}
{{< /tabs >}}

- En este caso `a` es cómo queremos nombrar a la variable/constante.
- Dependiendo de si es variable o constante, debemos usar el símbolo `:` | `=` según corresponda.
- En este caso `Entero` es el tipo de datos que se asocia a la variable/constante, podemos usar cualquiera de los mencionados anteriormente.

## Cómo nombrar variables y constantes

- Deben tener un nombre representativo.

    “a” es 💤 | “contpalabras” es 👼

- Además hay que tratar de abreviar las palabras claramente.

    “contpalimpar” 👍

- Y también…
    {{< details title="5 detalles" open=false >}}

- No pueden iniciar con números.

    `ej: 123var`
- No se distingue entre mayúsculas y minúsculas.

    `ej: var y VAR`
- No tener espacios.

    `ej: esto es un nombre incorrecto: Entero`
- No tener “símbolos raros”.

    `símbolos permitidos: “-” o “_”`
- No tiene que ser una palabra reservada

    `ej: leer, escribir`

{{< /details >}}
