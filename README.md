# patrones_de_diseño

## Principio de responsabilidad única

El principio de responsabilidad única es uno de los pilares de la construcción de software, establecido por Robert C. Martin. Este principio indica que una clase o función debe tener solo una razón para cambiar, lo que mejora la mantenibilidad y reduce la complejidad. Implementarlo no solo facilita las pruebas unitarias, sino que también incrementa la reutilización del código y disminuye el acoplamiento, promoviendo un sistema más cohesivo y fácil de escalar.

### ¿Qué implica el principio de responsabilidad única?

**Responsabilidad única:** Una clase o función debe encargarse de una única tarea, lo que evita que se ocupe de múltiples aspectos.

**Razón para cambiar:** El código debe tener una única causa para ser modificado, asegurando que los cambios sean claros y controlados.

### ¿Qué problemas soluciona este principio?

**Mantener el código:** Al dividir responsabilidades, el código se vuelve más fácil de mantener y más económico de modificar.

**Reutilización del código:** Las funciones con una única responsabilidad pueden ser utilizadas en diferentes contextos sin necesidad de duplicar código.

**Pruebas unitarias más simples:** Las funciones con responsabilidades bien definidas son más fáciles de probar, reduciendo la carga de trabajo en el desarrollo.

### ¿Cómo saber cuándo aplicar el principio de responsabilidad única?

**Múltiples razones para cambiar:** Si una clase o función tiene varias razones para ser modificada, es un buen indicio de que tiene más responsabilidades de las que debería.

**Alta complejidad y difícil mantenimiento:** Si se encuentra complicado añadir nuevas funcionalidades o corregir errores, es probable que la falta de una clara definición de responsabilidades esté afectando el código.

**Dificultad para realizar pruebas unitarias:** Si preparar una prueba implica mucho trabajo o configurar demasiados elementos, es señal de que el principio no se está siguiendo correctamente.

**Duplicación de código:** Si una funcionalidad, como una validación, está replicada en varios lugares, se debería extraer a una única función y reutilizarla donde sea necesario.

### ¿Qué hacer cuando encuentras duplicación de responsabilidades?

Cuando se identifica la duplicación de código o responsabilidades mal distribuidas, el enfoque ideal es reorganizar ese código en una función específica que pueda ser reutilizada en todos los puntos necesarios. Esto no solo reduce el trabajo redundante, sino que también asegura que los cambios futuros se realicen en un solo lugar.

Tenemos un ejemplo en la ruta ´src/srp´ donde el archivo before.py tiene una clase con muchas responsabilidades, y el archivo after.py tiene aplicado el principio de responsabilidad única