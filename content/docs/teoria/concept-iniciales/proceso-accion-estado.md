# Proceso, Acción y Estado

## Proceso

Un proceso, en su esencia más pura, es una diminuta entidad, cuidadosamente planificada por un Sistema Operativo, emerge como una unidad elemental de trabajo.

Formalmente:

{{< details title="Noun: Proceso /process/" open=true >}}
Una **unidad de actividad** que se caracteriza por la **ejecución de una secuencia** de instrucciones, un **estado actual**, y un **conjunto de recursos** de los sistemas asociados (hardware).
{{< /details >}}

## Acción

En el anterior "ejemplo 1" de algoritmos, notarás que cada paso comienza con un verbo como "Solicitar", "Ingresar", "Dividir", entre otros. Los verbos representan acciones, y todos sabemos que implican hacer algo.

Según la academia:

{{< details title="Noun: Acción /ac-yion/" open=true >}}
Es un **acontecimiento** producido por un **actor** que tiene un **tiempo finito** (período), produce un **resultado definido y preciso** y también produce un **cambio de estado**.
{{< /details >}}

Puede parecer contradictorio, pero "construir una casa" es una acción que está compuesta por otras acciones.

Las acciones se dividen en dos tipos: 

- simples, que se pueden hacer directamente.
- complejas, que requieren descomponerse en acciones más simples.

La percepción de lo que es simple o complejo varía de una persona a otra y depende de sus habilidades y del enfoque que le den al problema.

### Clasificación de Acciones

A lo largo de nuestro viaje por esta materia, desvelaremos los secretos de estas acciones. No obstante, debes comprender cuándo desatar cada tipo de acción en el momento preciso, es de vital importancia.

{{< mermaid >}}
stateDiagram-v2
    Acciones: Acciones
    Acciones --> Simples
    Simples: Simples
    Simples --> Asignación
    Asignación: Asignación
    Asignación --> Expresión
    Expresión: Expresión
    Expresión --> Incrementales
    Incrementales: Incrementales

    Incrementales --> Contador
    Contador: Contador
    Incrementales --> Acumulador
    Acumulador: Acumulador

    Expresión --> Algebraicas
    Algebraicas: Algebraicas
    Expresión --> Funcionales
    Funcionales: Funcionales

    Asignación --> Pura
    Pura: Pura

    Simples --> AcciónElemental
    AcciónElemental: Acción Elemental



    Acciones --> Estructuradas
    Estructuradas: Estructuradas
    Estructuradas --> Cíclicas
    Cíclicas: Cíclicas
    Cíclicas --> Pretest
    Pretest: Pre-test
    Cíclicas --> Posttest
    Posttest: Post-test
    Cíclicas --> Manejadaporcontador
    Manejadaporcontador: Manejada por contador

    Estructuradas --> Condicionales
    Condicionales: Condicionales
    Condicionales --> CondiSimples
    CondiSimples: Simples
    Condicionales --> Alternativos
    Alternativos: Alternativos
    Condicionales --> SelecciónMúltiple
    SelecciónMúltiple: Selección Múltiple

    Estructuradas --> Acciónconnombre
    Acciónconnombre: Acción con nombre
  
{{< /mermaid >}}

Aunque parezca abrumador, es crucial presentar todas las acciones en su conjunto para tener una visión global y comprensiva. De todas formas, voy a separarlas en dos grupos para que se puedan ver mejor. Comenzaré mostrando las simples:

{{< mermaid >}}
stateDiagram-v2
    Simples: Simples
    Simples --> Asignación
    Asignación: Asignación
    Asignación --> Expresión
    Expresión: Expresión
    Expresión --> Incrementales
    Incrementales: Incrementales

    Incrementales --> Contador
    Contador: Contador
    Incrementales --> Acumulador
    Acumulador: Acumulador

    Expresión --> Algebraicas
    Algebraicas: Algebraicas
    Expresión --> Funcionales
    Funcionales: Funcionales

    Asignación --> Pura
    Pura: Pura

    Simples --> AcciónElemental
    AcciónElemental: Acción Elemental
  
{{< /mermaid >}}

Y ahora las complejas o estructuradas:

{{< mermaid >}}
stateDiagram-v2
    Estructuradas: Estructuradas
    Estructuradas --> Cíclicas
    Cíclicas: Cíclicas
    Cíclicas --> Pretest
    Pretest: Pre-test
    Cíclicas --> Posttest
    Posttest: Post-test
    Cíclicas --> Manejadaporcontador
    Manejadaporcontador: Manejada por contador

    Estructuradas --> Condicionales
    Condicionales: Condicionales
    Condicionales --> CondiSimples
    CondiSimples: Simples
    Condicionales --> Alternativos
    Alternativos: Alternativos
    Condicionales --> SelecciónMúltiple
    SelecciónMúltiple: Selección Múltiple

    Estructuradas --> Acciónconnombre
    Acciónconnombre: Acción con nombre
  
{{< /mermaid >}}