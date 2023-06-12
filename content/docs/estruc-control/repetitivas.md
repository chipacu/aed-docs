---
title: Repetitivas
weight: 2
---

# Repetitivas

![waves](/aed-docs/images/infinite-waves.jpg)

Durante la creación de programas, es común encontrarse con la necesidad de repetir operaciones varias veces. Para esto, es importante conocer las estructuras de algoritmos que permiten la repetición de acciones un número determinado de veces.

{{< mermaid >}}
graph TB
    START:::hidden --> accion1
    accion1[Accion 1] --> input{Condición}
    input -- Verdadero --> execute[Instrucciones del Bucle]
    execute --> input
    input -- Falso --> accion2[Accion2]
    accion2 --> END:::hidden
{{< /mermaid >}}

Estas estructuras se llaman bucles y cada repetición del bucle se denomina iteración. Cada bucle debe tener una condición asociada que determina cuándo se repite y cuándo deja de repetirse.

{{< hint warning >}}
**♾️ Toda una Eternidad**  
Es importante tener cuidado con los bucles infinitos, que ocurren cuando la condición de finalización del bucle nunca se cumple.
{{< /hint >}}

## Pre-Test (while loop)

Se repite siempre que se cumpla una condición determinada. Es una estructura repetitiva de tipo indefinida, ya que no se conoce la cantidad exacta de veces que se repetirá el conjunto de instrucciones del bucle.

Si su condición inicialmente no se cumple, el bucle no se ejecuta.

```
MIENTRAS <cond> HACER
    <acciones>
FIN_MIENTRAS
```

## Post-Test

Similar a la anterior, pero la evaluación de la condición se encuentra al final, lo que garantiza que las acciones dentro del bucle se lleven a cabo al menos una vez, independientemente del valor de la condición.

Esta estructura también se considera indefinida y no está presente en la mayoría de los lenguajes de programación actuales, por lo que su uso se reemplaza generalmente con el ciclo "while".

```
REPETIR
    <acciones>
HASTA QUE <cond>
FIN_REPETIR
```

## Manejada por Contador (for loop)

Esta estructura es un ciclo definido, lo que significa que se conoce de antemano la cantidad exacta de veces que se iterará. El final del bucle está controlado por un contador y este se incrementa automáticamente según el incremento especificado.

En caso de que sea necesario un decremento, se indica con el signo `"--"`. Si el incremento o decremento es diferente a 1, se debe especificar. No es necesario inicializar la variable del contador.

```
PARA contador:=inicialización hasta fin; incremento HACER
    <acciones>
FIN_PARA
```

## Comparación entre Repetitivas

|                                                                         | Pre-test                                                                                                             | Post-test                                                                               | Manejado por contador                                |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|------------------------------------------------------|
| **Se deben conocer anticipadamente el número de Iteraciones?**          | No                                                                                                                   | No                                                                                      | Si                                                   |
| **En qué momento se verifica la condición?**                            | Antes de la ejecución del cuerpo del bucle                                                                           | Después de la ejecución del cuerpo del bucle                                            | Antes de la ejecución del cuerpo del bucle           |
| **Puede el bucle no ejecutarse nunca?**                                 | Si, si la condición es falsa la primera vez                                                                          | No, al menos una vez se ejecuta                                                         | Si, si **Vf<Vi en FOR_TO** o **Vi<Vf en FOR_DOWNTO** |
| **Se debe modificar el valor de la condición para finalizar el bucle?** | Si, haciendo que el valor de la condicion sea falsa                                                                  | Si, haciendo que el valor de la condición sea verdadera                                 | No, es automático                                    |
| **Un bucle puede ser infinito?**                                        | Si                                                                                                                   | Si                                                                                      | No                                                   |
| **Cuándo debe utilizarse?**                                             | El numero de iteraciones es indeterminado y no debe ejecutarse el bucle cuando la condición es falsa la primera vez. | El número de iteraciones es indeterminado y el bucle se debe ejecutar al menos una vez. | El número de iteraciones se conoce por adelantado.   |