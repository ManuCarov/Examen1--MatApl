Ejercicio 3

En el procesamiento de imágenes es fundamental identificar los bordes, ya que estos definen las formas y
estructuras presentes en una escena. En lugar de utilizar filtros tradicionales, exploraremos un enfoque
iterativo en el que cada píxel se actualiza en función de sus vecinos, hasta que la imagen alcanza un
estado estable. Este método, formulado como una ecuación de punto fijo, te permitirá comprender cómo
la iteración puede realzar los bordes de manera progresiva.
Implementarás un algoritmo iterativo basado en la siguiente regla que esta adjuntada.

donde X^(n) es la imagen en la iteración n y α es un parámetro que hay que ajustar.

Tareas
1. Interpretación del algoritmo: A partir del proceso iterativo presentado ¿cómo cambia la imagen
en cada iteración? ¿cómo se obtiene la imagen con los bordes? ¿Qué controla α?
2. Modelado: Comienza con una imagen en escala de grises X0 y utiliza la regla iterativa para
actualizar los píxeles.

3. Implementación: Programa1 el proceso iterativo hasta que la diferencia entre iteraciones consecutivas sea menor que un umbral. Debe justificar la métrica que va a usar y cómo la va a usar. Experimenta con distintos valores de α y con diferentes imágenes. En la implementación debe usar la menor cantidad de bucles for posibles.

4. Análisis: A partir del gráfico del error (o modificaciones convenientes del error) en función del
número de iteraciones n, determine si la tasa de convergencia se comporta de manera exponencial
(por ejemplo, O(e^(−λn)) para algún λ > 0) o si pudiera ajustarse a una tasa polinomial (por ejemplo,
O(1/n^c) para algún c > 0).

-------------------------------------------------------------------------------------------------------------------------------

1. El script de Python debe aceptar cualquier imagen en escala de grises y entregar por lo menos la imagen original y la
imagen con los bordes.
2. Advertencia: El algoritmo descrito produce una imagen suavizada, para encontrar la imagen con los bordes requeridos
se necesita hacer algo mas.
3Nota sobre la notación O (Big-O) y la velocidad de convergencia: En clase vimos que algunas sucesiones
convergen a su límite más rápido que otras. La notación O(·) es una forma matemática de clasificar esa “velocidad” de caída.
Decir que el error es O(e
−λn) significa que la magnitud del error se encoge a un ritmo proporcional a e
−λn (una convergencia
exponencial, muy rápida). Por otro lado, decir que es O(1/n
c
) significa que el error decae proporcionalmente a 1/n
c
(una
convergencia polinomial, que es mucho más lenta). Para su análisis, observen si en su gráfica el error cae de golpe hacia cero
o si lo hace de manera más suave y prolongada