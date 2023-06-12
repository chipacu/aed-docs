---
title: Pseudocódigo
weight: 4
---

# Pseudocódigo

![lapiz y papel](/aed-docs/images/retro-notepad.jpg)

Los algoritmos trascienden a los lenguajes de programación, pudiendose representar de diversas maneras. En esta cursada, solo nos centraremos en el *pseudocódigo*, pero pueden investigar sobre las demás formas por su cuenta.

Pero entonces ¿qué es ese tal pseudocódigo?

{{< details title="Noun: Pseudocódigo /pseudo/" open=true >}}
Es un lenguaje similar al inglés utilizado para **representar estructuras de control** en `programación estructurada`.

Aunque es un primer borrador, **debe traducirse** a un lenguaje de programación para ser ejecutado en una computadora.
{{< /details >}}

¿Y qué es esa programación estructurada?

La programación estructurada es un enfoque metódico y científico para diseñar y escribir programas, alejándose del método de prueba y error.

Se fundamenta en dos aspectos clave:

1. Las **Características de un Algoritmo**

{{< mermaid >}}
stateDiagram-v2
    Uno: 1. Posee un solo punto de Entrada y de salida.
    Uno --> Dos
    Dos: 2. Todas las acciones deben ser accesibles.
    note right of Dos
        Debe haber al menos un camino
        desde el principio hasta el
        final que pase por cada accion.
    end note
    Dos --> Tres
    Tres: 3. No posee ciclos o bucles infinitos.
  
{{< /mermaid >}}

2. El **Teorema de la Programación Estructurada**: postula que todo algoritmo estructurado puede ser escrito utilizando únicamente tres tipos de estructuras de control secuenciales.

- Secuenciales
- Condicionales
- Repetitivas

{{< expand "Pseudocódigo vs Diagramas de Flujo" "..." >}}
El uso de Pseudocódigo en lugar de Diagramas de Flujo tiene ventajas, como la capacidad de representar de manera sencilla operaciones repetitivas complejas. Además, es fácil convertir una solución en Pseudocódigo a un programa en cualquier lenguaje de programación. Siguiendo las reglas, se pueden visualizar claramente los niveles de cada operación.
{{< /expand >}}