# Lectura 2: Matrix Factorization Techniques for Recommender Systems

<center>Yehuda Koren, Yahoo Research </center>
<center>Robert Bell and Chris Volinsky, AT&T Labs—Research</center>


-----
## Resumen

Las técnicas de recomendación basadas en la factorización matricial tiene varias ventajas respecto a las técnicas de filtrado colaborativo.Existen dos grupos de técnicas, las basadas en la vecindad: Se basa en *juntar* items con evaluación similar por parte de un usuario o usuarios según su rating a cierto item. El otro grupo son los modelos de factores latentes, que consisten en proyectar items y usuarios a un mismo espacio vectorial, donde las dimensiones representa una especie de **variable oculta**, que puede no ser entendible para el humano, pero que permite categorizar los items y usuarios.

Los factores latentes pueden ser implementados mediante técnicas de factorización matricial. En particular se usa la Descomposición en Valores Singulares que permite trabajar con sets con más items que usuarios o al revés. Con esta descomposición (Aplicando una reducción de dimensionalidad arbitraria) se procede a resolver un problema de mínimos cuadrados para poder predecir los ratings de los usuarios. En este punto, se aplica también un proceso conocido como regularización que permite evitar un sobre entrenamiento del modelo. El problema de mínimos cuadrados puede ser resuelto con dos métodos: ALS (Alternating Least Squares) y Descenso estocástico del grandiente.

El uso de matrices resultan buenos a la hora de eliminar sesgos (Un item que tienda a ser bien evaluado, un usuario que evalue todo bien o todo mal), además que permite mayor libertad al permitir modificar el rating o añadir nuevas valoraciones evitando tener que recalcular todo de nuevo.

## Comentarios

Los métodos que usan factorización matricial que se muestran en la lectura presentan significativas ventajas respecto a los métodos colaborativos.

Entre las que más destaco, considero que para términos de aplicabilidad es importante que trabaje con menos dimensiones que la matriz original, esto hace más factible tenerla en memoria o evita tener que hacer una copia de una especie de producto cruz de la base de datos. Del mismo modo, resolver el problema de modificación de datos creo que es importante que lo resuelva para poder ser aplicado en un sistema real.

Otro importante avance que llamó la atención es que se eliminan ciertos sesgos asociados a una determinada manera que tiene un ítem de recibir un ranking, o de un usuario de evaluar bien o mal. Me parece importante que se haga énfasis en este tema, que es un problema si tenían los sistemas colaborativos. Me parece que este factor es muy importante que lo aborden, por la dificultad intrínseca que estos tienen, en la vida real lo veo análogo al problema de decidir entre dos recomendaciones u opiniones opuestas.

Finalmente, un aspecto que ya se ha hablado de todas maneras, es que los modelos basados en factores latentes mapean a un espacio en el que no puedo interpretar las dimensiones, por ende no puedo saber en base a que está recomendando. Si a esto se le añaden técnicas de recopilación de ranking ímplicitas o simplemente meto más variables  que solo el ranking de una película al modelo ¿Podría el modelo efectuar algún tipo de discriminación?.


