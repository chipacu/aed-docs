---
title: Tipos de Datos
weight: 1
---

# Tipos de datos

![mago levitando cosas](/aed-docs/images/datatypes.jpg)

En esta etapa inicial, nos enfocaremos en algunos tipos de datos fundamentales, esto solo por ahora, más adelante la cosa se complica.

## Numericos

Iniciaremos contando un chiste... se dice que, *si Dios es Real, es porque no lo declararon como Entero.*

Ya está loco, los perdí para siempre... estos tipos de datos representan números, y más abajo veremos porqué se los categorizan en dos partes.

### Enteros

Son un conjunto finito de valores que no contienen partes fraccionarias o decimales, y pueden ser tanto positivos como negativos. Se utilizan para representar cantidades completas, como la edad de una persona, que siempre se considera un valor entero.

**Ejemplo**:

```
4 | 434 | 565546 | ...
```

### Reales

Son un subconjunto de los números reales que siempre incluyen un punto decimal y pueden ser positivos o negativos. Se utilizan para representar valores que tienen componentes fraccionarios, como el peso de una persona.

**Ejemplo**:

```
3.14 | 12838.49586 | ...
```

En la mayoría de los lenguajes de programación, es necesario utilizar el punto `(.)` en lugar de la coma `(,)` al escribir números reales. Esto se debe a que estos lenguajes están inspirados en el inglés y utilizan esa sintaxis. Se recomienda seguir esta convención al escribir pseudocódigo también, aunque desconozco su obligatoriedad.

...

{{< hint info >}}
**🤔 ¿Por qué el énfasis en diferenciar los datos numéricos?**  
Más adelante, nos encontraremos con operadores específicos que diferencian entre la division entera y real. Esto probablemente se deba a que las computadoras a bajo nivel sean malas a la hora de trabajar con la matemática contínua (opuesta a la discreta).
{{< /hint >}}

## Alfanumericos

En una presentación del profe Axel, se mencionaban a los alfanuméricos como un conjunto de caracteres.

**Ejemplo**:

```
"hola señor kiosquero..." | "192./aa321" | "rm -rf /" | "&asd" | ...
```

Y a estos, se les puede especificar su longitud de la siguiente forma:

```
Alfanumérico(20) o AN(20)
```

En este caso, se quiere que el limite de carácteres sea 20.

### Carácter

Cuando se piensa, en cada letra, número o símbolo solitario, la figura del "carácter" emerge ante nosotros.

**Ejemplo**:

```
"1" | "a" | "B" | "&" | ...
```

## Lógicos o Booleanos

El tipo de dato que solo puede tener dos valores: Falso ❌ y verdadero ✔️. Se utiliza, por ejemplo, cuando se desea determinar si un número es primo o no.

Ejemplo:

```
Verdadero | Falso
```