---
title: Estructura Básica Pseudocódigo
weight: 5
---

# Estructura Básica Pseudocódigo

Una vez tengas tu editor de código y estes medio familiarizado con los conceptos básicos de pseudocódigo y sus elementos, vas a estar listo para enfrentarte a los primeros ejercicios del práctica.

Bueno, quizás no, te faltan las partes más importantes, la estructura que funje como esqueleto de tu algorítmo.

```
Accion Un_ejemplo es
    Ambiente
        // aquí se declaran variables/c, se definen funciones/p...
    Algoritmo
        // donde ocurre la magia...
fin accion
```

Quizas aquí no quede muy en claro cómo usarla porque solo la describí, podría desarrollar unos cuantos algorítmos e irlos comparando, pero será mucho mejor que los veas por tu cuenta en el repostorio de ejercicios resueltos.

## Cuidado con la indentación

La «indentación» en criollo, es cuando nos referirnos a la **sangría** del código. Por ahora no es indispensable, pero si se recomienda usarla, es un horror ver el código todo descuajeringado.

Mirá y comparalo por tu cuenta...

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

La cantidad de espacios varía dependiendo del lenguaje y los estándares que uses, recomiendo usar 4 espacios que es la opción que viene por defecto en la mayoría de editores modernos.

{{< /tab >}}
{{< /tabs >}}

## Comentarios

Todo texto que se escriba después de // es un comentario, y no afecta en la ejecución del código.

```
// soy un comentario
no soy un comentario
```

Los programadores buscan constantemente la perfección, pero la mente humana puede ser olvidadiza. Documentar el código se vuelve invaluable, especialmente cuando otros lo revisan. Como portadores de estos conocimientos, debemos perseverar en esta tarea. No escatimes en comentarios, ya que son esenciales para la comprensión y comunicación.