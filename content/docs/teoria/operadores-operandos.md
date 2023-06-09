# Operadores y Operandos

Los programas de computadora se basan en la realización de muchas operaciones aritméticas y matemáticas de diversas complejidades.

{{< details title="Noun: Operador /operasao/" open=true >}}
Es el símbolo que **determina el tipo de operación o relación** que habrá de establecerse entre los operandos para alcanzar un resultado.
{{< /details >}}

Los operadores nos permiten manipular datos, ya sean variables, constantes u otras expresiones. Podemos utilizarlos para `transformar` datos, `controlar el flujo` de ejecución de un programa mediante decisiones y `formar valores para asignar` a otros datos.

{{< hint info >}}
**👁️ Ojito:**
El *tipo de datos* utilizado en una **expresión** *está relacionado* con los operadores utilizados.
{{< /hint >}}

Y ¿Qué son esas expresiones mencionadas?

{{< details title="Noun: Expresión /exprasao/" open=true >}}
Es en síntesis, una secuencia de **operadores y operandos** que realizan un **cálculo**.
{{< /details >}}

**Ejemplo**: `3x2`; En esta expresión, el símbolo `x` se utiliza como el operador de multiplicación, mientras que los números `3` y `2` son los operandos involucrados en la operación.

Hay varios tipos de operadores disponibles:

## Operador de Asignación

Es el más básico y se utiliza para asignar un valor a una variable. En muchos lenguajes de programación, se representa con el símbolo `:=`. Este operador indica que el valor a la derecha de `:=` será asignado a la variable que está a la izquierda del mismo.

**Ejemplo**:

```
Edad := 29
precio := 25.45
```

Acordate que la acción de asignar es destructiva 💣, ya que el valor que tuviera la variable antes de la asignación se pierde y se reemplaza por el nuevo valor.

## Operadores Aritméticos

Son operadores binarios, lo que significa que requieren dos operandos para funcionar. Estos operadores realizan las **operaciones aritméticas básicas** y utilizan operandos numéricos para proporcionar resultados matemáticos.

| Operador | Descripción              |
|----------|--------------------------|
| +        | Suma                     |
| -        | Resta                    |
| *        | Multiplicación           |
| /        | División Real            |
| mod      | Resto División Entera    |
| div      | Cociente División Entera |
| **       | Porenciación             |

## Operadores Relacionales

Se utilizan para realizar comparaciones de igualdad, desigualdad y relaciones de menor o mayor entre valores. Estos operadores son utilizados para expresar condiciones en algoritmos y proporcionan resultados lógicos.

| Operador | Significado       |
|----------|-------------------|
| =        | Igual a           |
| <>       | No Igual a        |
| >        | Mayor que         |
| >=       | Mayor o Igual que |
| <        | Menor que         |
| <=       | Menor o Igual que |

{{< hint info >}}
**💡 Trucazo:**
Para recordar cómo funcionan los operadores de menor y mayor se puede imaginar que el símbolo se asemeja a un pico de pato y que los ojos del pato están en el punto donde se cruzan las líneas `''< cuak!`. Recordá que el pato siempre mira al operando más grande `🟡🔵 >''`. Este truco puede ser útil si alguien pasó la primaria por acomodo o debido a la pandemia y no está familiarizado con estos operadores.
{{< /hint >}}

Acordate también que no existe el operador `≠`.

# Operadores Lógicos

Los operadores lógicos, nos permiten tomar decisiones basadas en la
verdad y la falsedad de las proposiciones. Nos guían a través del
laberinto de la lógica y nos permiten construir algoritmos que actúan
con discernimiento.

|    Operador   |     Descripción     |  Uso  |
|:-------------:|---------------------|:-----:|
| AND \| ᴧ \| Y | Operador lógico AND | a Y b |
| OR \| ᴠ \| O  | Operador lógico OR  | a O b |
|       NO      | Operador de Negación| a NO b|

Y las tablas de verdad de los mismos:

{{< tabs "uniqueid" >}}
{{< tab "Disyunción" >}}

|     A    |     B    |   `A o B`  |
|:--------:|:--------:|:--------:|
| Falso ❌  | Falso ❌  | Falso ❌  |
| Falso ❌  | Verdad ✔ | Verdad ✔ |
| Verdad ✔ | Falso ❌  | Verdad ✔ |
| Verdad ✔ | Verdad ✔ | Verdad ✔ |

{{< /tab >}}
{{< tab "Conjunción" >}}

|     A    |     B    |   `A y B`  |
|:--------:|:--------:|:--------:|
| Falso ❌  | Falso ❌  | Falso ❌  |
| Falso ❌  | Verdad ✔ | Falso ❌  |
| Verdad ✔ | Falso ❌  | Falso ❌  |
| Verdad ✔ | Verdad ✔ | Verdad ✔ |

{{< /tab >}}
{{< tab "Negación" >}}

|     A    |   `No(A)`  |
|:--------:|:--------:|
| Falso ❌  | Verdad ✔ |
| Verdad ✔ | Falso ❌  |

{{< /tab >}}
{{< /tabs >}}

## Prioridad de los Operadores

La precedencia (orden de resolución) funciona similar al de las matemáticas:

| Operadores           | Descripción                                                |
|----------------------|------------------------------------------------------------|
| + \| - \| no         | Signo más, Signo menos y Negación                          |
| **                   | Potencia                                                   |
| * \| / \| div \| mod | Multiplicación, División real, División entera y Módulo    |
| + \| -               | Suma y Resta                                               |
| +                    | Concatenación                                              |
| < \| <= \| > \| >=   | Menor que, Menor o igual que, Mayor que, Mayor o igual que |
| = \| <>              | Igual que y Distinto que                                   |
| y                    | Conjunción                                                 |
| o                    | Disyunción                                                 |