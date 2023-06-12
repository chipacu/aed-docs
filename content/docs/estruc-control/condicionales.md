---
title: Condicionales
weight: 1
---

# Condicionales

![two way path](/aed-docs/images/two-way-path.jpg)

Hasta este punto, los algoritmos que hemos definido se ejecutan de manera **secuencial**, es decir, una sentencia después de otra. Esta forma de programación es adecuada para programas simples.

{{< mermaid >}}
flowchart LR
    START:::hidden --> accion1
    accion1[Acción 1]
    accion1 --> accion2
    accion2[Acción 2]
    accion2 --> STOP:::hidden

    classDef hidden display: none;
  
{{< /mermaid >}}

```
ACCION Ejemplo1 ES
AMBIENTE
    a,doble: entero
PROCESO
    ESCRIBIR(“Ingrese el número: ”)
    LEER(a)
    doble := a * 2
    ESCRIBIR(“Resultado es: ”,doble)
FIN_ACCION
```

Sin embargo, para resolver problemas más complejos, es necesario tener la capacidad de controlar qué sentencias se ejecutan y cuándo. El hecho de que las acciones se ejecuten secuencialmente implica que nunca se ejecutará más de una acción al mismo tiempo.

Las **estructuras selectivas**, también conocidas como estructuras de decisión o alternativas, se utilizan para tomar decisiones lógicas.

La estructura condicional es útil cuando cuando hay diferentes alternativas que dependen de la evaluación de una condición específica.


{{< mermaid >}}
flowchart TB
    START:::hidden --> accion1
    accion1[Acción 1]
    accion1 --> accion2
    accion2[Acción 2]
    accion2 --> condic1
    condic1{Condición}
    accion3[Acción 3]
    accion4[Acción 4]
    condic1-->|No|accion3
    condic1-->|Si|accion4
    accion3 --> STOP:::hidden
    accion4 --> STOP2:::hidden

    classDef hidden display: none;
  
{{< /mermaid >}}

## Alternativo Simple

La estructura condicional más simple es aquella que permite implementar acciones condicionales de la siguiente manera:

1. Si una determinada condición **se cumple**, se ejecutan una serie de instrucciones y luego se continúa con el flujo del programa.
2. Si la condición **NO se cumple**, las instrucciones no se ejecutan y se sigue adelante.

Una vez evaluada la expresión condicional, el programa recupera su flujo secuencial y continúa ejecutando las instrucciones siguientes.

```
ACCION Ejemplo2 ES
AMBIENTE
    a:entero
PROCESO
    ESC(“Ingrese el número: ”)
    LEER(a)
    SI a > 0 ENTONCES:
        ESCRIBIR(“El nro. es positivo”)
    FIN_SI
FIN_ACCION
```

## Alternativo Doble

La estructura condicional alternativa doble permite implementar condicionales en los que hay dos acciones alternativas:

1. Si **se cumple** una determinada condición, se ejecuta un bloque de instrucciones (bloque 1).
2. Si la condición **NO se cumple**, se **ejecuta otro bloque** de instrucciones (bloque 2).

```
ACCION Ejemplo3 ES
AMBIENTE
    A,B:ENTERO
PROCESO
    ESC(“Ingrese el primer número: ”), LEER(A)
    ESC(“Ingrese el segundo número: ”), LEER(B)
    SI A > B ENTONCES
        ESC(A,“es mayor que “,B)
    SINO
        ESC(A,“NO es mayor que “,B)
    FIN_SI
FIN_ACCION
```

{{< hint info >}}
**💁‍♂️ Anidar Condicionales en forma de Cascada**  
Si una condición no se cumple, se puede utilizar el bloque "sino" para definir otro condicional. Esto nos permite crear estructuras más complejas y tomar decisiones adicionales en función de diferentes condiciones.

```
SI Falso ENTONCES
    ESC("Esto no va a pasar")
SINO
    SI Falso ENTONCES
        ESC("Esto no va a pasar")
    SINO
        SI Falso ENTONCES
            ESC("Esto no va a pasar")
        SINO
            ∞
        FIN_SI
    FIN_SI
FIN_SI
```

{{< /hint >}}

## Alternativo Múltiple

Es utilizada cuando existen **más de dos elecciones**. En lugar de utilizar estructuras alternativas simples o dobles anidadas, se recomienda utilizar esta estructura para mejorar la legibilidad del código cuando el número de alternativas es grande.

En esta estructura, se evalúa una variable que puede tomar de 1 a n valores diferentes. Dependiendo del valor que tome la variable, se ejecutará una de las n acciones correspondientes.

```
ACCION EJEMPLO4 ES
AMBIENTE
    a,b,suma: entero
PROCESO
    ESC(“Ingrese el primer número”), LEER(a)
    ESC (“Ingrese el segundo número”),LEER(b)
    suma := a + b
    SEGÚN suma HACER
        =0 : ESC(“El resultado es igual a 0”)
        <0: ESC(“El resultado es menor a 0”)
        >0: ESC(“El resultado es mayor a 0”)
    FIN_SEGUN
FIN_ACCION
```

Y esta también puede ser escrita usando los alternativos dobles vistos anteriormente:

```
ACCION OtroMas ES
AMBIENTE
    a,b,suma:entero
PROCESO
    ESC(“Ingrese el primer número”), LEER(a)
    ESC (“Ingrese el segundo número”),LEER(b)
    suma := a + b
    SI suma = 0 ENTONCES
        ESC(“El resultado de la suma es 0”)
    SINO:
        SI suma < 0 ENTONCES
            ESC(“El resultado de la suma es menor a 0”)
        SINO:
            ESC(“El resultado de la suma es mayor a 0”)
        FIN_SI
    FIN_SI
FIN_ACCION
```