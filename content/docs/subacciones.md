---
title: 🚧 Subacciones
weight: 8
---

# Subacciones

![en construcción](/aed-docs/under-construction.jpg)

La resolución de problemas complejos se simplifica al dividirlos en problemas más pequeños. Estos subproblemas se resuelven utilizando subalgoritmos o subacciones.

![ejemplo subacciones](/aed-docs/images/subacciones-intro.png)

{{< details title="Subacciones o Subalgoritmos" open=true >}}
- Son acciones que **forman parte** de una accion principal.
- Son módulos que están escritos para ejecutar alguna **tarea específica**.
- Se definen en el **ambiente** pues van a ser utilizadas e invocadas durante el
**proceso** del algoritmo diseñado.
- Se **escriben solamente una vez**, pero pueden ser referenciados en
diferentes puntos del algoritmo, de modo que se puede evitar la
duplicación innecesaria del código.
{{< /details >}}

## Control de Ejecución

El algoritmo principal se ejecuta primero, luego ordena la ejecución de un subalgoritmo.

Cuando se realiza esa solicitud, el algoritmo principal se detiene hasta que el subalgoritmo haya completado sus tareas, para luego retomar la ejecución.

A este proceso se le llama control de ejecución y puede suceder n veces.

## Elementos de Subacciones

### Nombre

Las subacciones se definen mediante un nombre único que representa el objetivo específico del subalgoritmo. Estos nombres no deben ser palabras reservadas como "Escribir" o "Leer".

### Parámetros

A veces las subacciones necesitan pasar o recibir datos de/a la acción principal para ejecutarse. Los **parámetros** son variables/constantes utilizados para estas labores.

Existen dos tipos:

- **Formales o ficticios**: son los que aparecen en la definición del subalgoritmo.
- **Actuales o argumentos**: Son los que el algorítmo principal envía desde la llamada al subalgoritmo, contiene los valores para evaluar el subalgoritmo en ese momento.

{{< hint info >}}
Los parámetros actuales pueden ser constantes, variables, expresiones. En
cambio, los parámetros formales sólo pueden ser variables.
{{< /hint >}}

Cuando un algoritmo llama a una subacción, se establece una correspondencia entre los argumentos y los parámetros formales. Se verifica que la cantidad de parámetros sea la misma y que los tipos de datos coincidan en el orden definido. En ejemplos posteriores se ilustrará esta cuestión para una mejor comprensión.

## Funciones

{{< details title="Definición" open=true >}}
Una función es un subalgoritmo que recibe datos de tipo numérico o no numérico como argumentos o parámetros actuales y devuelve un único resultado.
{{< /details >}}

Existen dos tipos:
- Internas: son las que ya vienen incorporadas al sistema.
- Externas: las que son definidas por el usuario.

Y así es como se las declara:

```
Funcion nombrefunc(<lista_de_parámetros>) : <tipo>

// declaraciones locales si fuera necesario > ambiente

// acciones de la funcion

nombrefunc := <valor de la función> // se necesita para que devuelva un valor
Fin Funcion
```

- `nombrefun` : es el nombre de la función.
- `lista de parámetros` : es la lista de parámetros formales. **Esta lista no puede ser vacía**.
- `tipo`: es el tipo de resultado que devuelve la función.

El algoritmo principal llama a una función utilizando su nombre seguido de una lista de argumentos que deben coincidir en cantidad, tipo y orden con los parámetros definidos en la función. Para ejecutar las acciones descritas en una función, esta debe ser invocada desde el algoritmo principal o desde otros subalgoritmos, proporcionándole los argumentos de entrada necesarios para realizar esas acciones.

Ejemplo de función:

```
FUNCION ES_PRIMO(A:entero):lógico
    AMBIENTE
        i: entero
    PROCESO
    ES_PRIMO := V // habilito la función como bandera
    PARA i := 2 hasta (A-1) HACER
        SI A mod i = 0 ENTONCES
            ES_PRIMO := F // ya no es primo
        FIN_SI
    FIN_PARA
FIN_FUNCION
```

## Procedimientos

{{< details title="Definición" open=true >}}
Un procedimiento es una subacción con un propósito específico, pero a diferencia de las funciones, no devuelve ningún valor, solo ejecuta acciones.
{{< /details >}}

Un ejemplo:

```
PROCEDIMIENTO Login(usu,pass,valid:alfanumerico)
    Si pass = valid entonces
        ESC(‘Acceso autorizado a ‘, usu)
    Sino
        Esc(‘Login inválido para ‘, usu)
    FinSi
FIN_PROCEDIMIENTO
```

¿Por qué usar procedimientos?

- Facilita el [diseño top-down](https://es.wikipedia.org/wiki/Top-down_y_bottom-up) de las soluciones.
- Las definís una vez, las usás las veces que quieras.
- Facilita la división de tareas.

## Ámbito de Variables

El ámbito de las variables se refiere a las partes del algoritmo en las que una variable es reconocida.

{{< columns >}}

### Variables Locales

Son las variables declaradas dentro de una subacción. Se crean cuando la subacción es llamada por el algoritmo principal y se destruyen al finalizar la ejecución de esa subacción.

<--->

### Variables globales

Son las variables declaradas en el algoritmo principal. Pueden ser utilizadas tanto en el algoritmo principal como en todas las subacciones declaradas dentro de él.

{{< /columns >}}

## Paso de Parámetros

Es cuando el algoritmo principal envía variables a una función o procedimiento para que trabajen con ellos internamente.

Hay dos alternativas para pasar los parámetros:

- **Paso por valor**
- **Paso por referencia**

### Detalles del paso por valor

Falta resumir y checkear esto

Cuando surge la necesidad de obtener el valor o contenido de una variable local desde el
algoritmo principal hacia una subacción, se está utilizando la estrategia de paso de parámetros
por valor.
En este caso se produce una copia de la variable original hacia el argumento formal de la función o
procedimiento que lo recibe. Dicha variable tendrá como ámbito la función receptora o
procedimiento receptor y al culminar su ejecución se liberará el espacio de memoria que ocupa.
Si usamos parámetros por valor, nunca podremos modificar los valores de las variables originales
ya que se producen copias de las mismas hacia las variables de la función llamada y su ámbito es
local.

Aquí va un cuadro