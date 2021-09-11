# Lectura 4: Content-Based Recomendation Systems

<center>Michael J. Pazzani</center>
<center>Daniel Billsus</center>


-----
## Resumen

Existen escenarios, usar la descripción de un item puede ser más preciso que usar una recomendación basada en feedback implicito o colaborativo. Por ejemplo dos usuarios que consumen lo mismo, excepto en la sección de golosinas, donde uno siempre busca algo salado y el otro dulce, bajo las técnicas ya vista, sonaría lógico que el sistema recomendara algo salado al que busca dulce y algo dulce al que busca salado, pues si tienen gustos similares, bajo la lógica de esos modelos, debería gustarle la recomendación. Sin embargo en la realidad claramente no es así, lo que se busca en un sistema que recomiende productos de sabor dulce al que siempre compra dulce y salado al que siempre compra salado.

Para lograr esto, primero se debe contar con una representación estructurada de cada item y por otra parte una representación del perfil de usuario (Intereses + historial).

Finalmente, al hora de entrenar estos modelos, se debe tener precacución en separar para un usuarios los items en dos categorías: Los que le gustaron/compró, etc, la otra categoría sería la de los items que no le fueron de interés. Para entrenar estos modelos se usan modelos como Árboles de Decisión, KNN, Clasificadores Lineares, Bayesianos, etc.



## Comentarios

Uno de las principales limitaciones de la recomendación basada en contenido es en generar los perfiles de items principalmente. En particular, si se piensa en una base de datos estructurada (Tipo SQL por ejemplo), implica pensar en todos los atributos que pueden ser de utilidad para la recomendación, lo que es difícil pensarlo en una primera implementación, por ende, esto implica que se deben añadir columnas cuando el sistema ya está en marcha, pero esto genera valores nulos y puede entorpercer la recomendación. Por otra parte, los textos libres no se pueden representar de manera estructurada manteniendo la totalidad de su semántica, lo que resulta en que la descripción no es tan efectiva.


Sin embargo, como se menciona al final del artículo, una ventaja o un caso de uso es que se pueden usar en conjunto con otra técnica, para ordenar el output de las recomendaciones basadas en el contenido por ejemplo, no habría problema en no contar con una buena descripción de los items, pues el conjunto de items a recomendar/ordenar/etc, ya tiene una alta probabilidad de cumplir con las necesidades del usuario.