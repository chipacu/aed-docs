# Prueba de escritorio

Es una forma de verificar la precisión y efectividad de un algoritmo mediante la **simulación manual de su ejecución** con **datos de entrada predefinidos**.

La prueba de escritorio garantiza la calidad del programa, mejora la comprensión y promueve el crecimiento del programador.

## Para elaborar una Prueba de Escritorio

Se utiliza una tabla con encabezados que representan las variables utilizadas en el algoritmo. Se van llenando los valores que toman estas variables, paso a paso, siguiendo el flujo indicado por el algoritmo hasta llegar al final. Cada fila de la tabla representa el estado de las variables en un momento específico.

|                      | Estado          | a     | b     | suma  |
|----------------------|-----------------|-------|-------|-------|
| 1. `a := 2;`           | E0 = Einicial   | ?     | ?     | ?     |
| 2. `b := 3;`           | E1              | 2     | ?     | ?     |
| 3. `suma := a + b;`    | E2              | 2     | 3     | ?     |
| 4. `suma := suma - 1;` | E3              | 2     | 3     | 5     |
|                      | **E4 = Efinal** | **2** | **3** | **4** |



{{< details title="La prueba consta de dos etapas:" open=true >}}
La primera prueba el programa con datos fáciles, la segunda busca datos que hagan fallar el algoritmo para detectar errores adicionales. Si el algoritmo no falla, se considera correcto y terminado.
{{< /details >}}