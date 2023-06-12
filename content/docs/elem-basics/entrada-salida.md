---
title: Entrada y Salida de Datos
weight: 4
---

# Entradas y Salida de Datos

Son dos **acciones con nombre** que se emplean en los primeros algoritmos. La información que compartiré a continuación está basada en las presentaciones de las clases prácticas, así como en algunos recursos de las clases de teoría.

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