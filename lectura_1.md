# Lectura 1: Collaborative Filtering Recommender Systems

<center>Ben Schafer, Dan Frankowski, Jon Herlocker, and Shilad Sen</center>

-----
## Resumen
En el paper se discuten acerca de los sistemas recomendadores colaborativos (Collaborative Systems o CF). La idea de estos sistemas nace de manera en la que un círculo de amigos de una persona puede afectar su comportamiento para consumir o no consumir un determinado producto.

Los CF trabajan sobre un conjunto de datos formado por usuarios, cada uno de estos tiene una valoración sobre todos los items. Luego el CF debe *recomendar un conjunto de items a un usuario*, *predecir el comportamiento del usuario respecto a un item*, etc. Existen diversar manera de obtener un rating, así como también algoritmos para realizar la recomendación o predicción en sí mismo que se han desarrollado a lo largo de los años.

## Comentarios

Uno de los aspectos que más llamó mi atención fue la descripción del dominio sobre el que los CF pueden trabajar. En particular hubo un punto que se refería a la similitud de los items en el ámbito objetivo, creo que este es un factor limitante.

Entiendo que al momento de hablar de sistemas recomendadores, una tarea básica o primaria es recomendar películas, canciones, etc, pero siempre a partir de *lo mismo*, Es decir, recomendar películas a partir de películas que he visto. En este aspecto creo que los CF atacan bien este problema, pero veo grandes dificultades a la hora de recomendar items distintos, como por ejemplo ropa a partir de música. En particular limitante que veo es que la métrica del rating puede ser la misma para clases de objetos, pero no necesariamente la percepción del usuario es la misma. Por ejemplo, en una escala de 1-5 una canción que reciba un 3, puede deberse a que la canción en sí no es mala, sino que era más de lo mismo de este artista, pero la canción es buena o vale la pena escucharla, sin embargo un 3 en un restaurant puede significar una mala experiencia y por ende un llamado a no ir. La canción y el restaurant tienen la misma nota, pero una valoración muy distinta.


Considero que el desarrollo teórico sobre los CF es suficiente para desarrollarlos como una técnica robusta (Abarca desde la obtención de rankings, obtenición de la recomendación y evaluación del desempeño del sistema). Eso no significa que existan limitantes computacionales (costo en cómputo), sociales (usuarios no emiten rankings), éticas (hasta que punto puedo obtener valoraciones de manera implícita) y otras como las que discutí en el párrafo anterior. Es por esto que creo que está bastante claro lo que se puede y no se puede hacer con un CF, y es necesario buscar otras técnicas si se quieren superar dichas limitantes.

