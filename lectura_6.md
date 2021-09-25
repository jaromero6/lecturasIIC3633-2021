# Lectura 6: Deep learning based recommender system: A survey and new perspectives

<center>Zhang, S.</center>
<center>Yao, L.</center>
<center>Sun, A.</center>
<center>Tay, Y.</center>


-----
## Resumen

El Aprendizaje Profundo ha tenido éxitos importantes en diversas áreas o problemas de computación
en la última década. Es por esto que se ha comenzado a usar en el área de Recomendación en reemplazo de las técnicas más clásicas (basadas en colaboración y contenido). Estas técnicas (CNN, RNN, MLP, etc) ofrecen un mayor potencial por su flexibilidad para procesar la información que reciben como input, aunque tiene limitaciones, pues requiere de una gran cantidad de datos de entrenamiento, dificultad de interpretación de su funcionamiento y la cantidad de hiperparámetros que se deben ajustar.

## Comentarios

Creo que el aprendizaje profundo tiene sumamente mayor potencial que las técnicas vistas anteriormente, pues los supuestos que estaban detrás se esas técnicas se pueden aplicar también en los modelos de aprendizaje profundo, sin embargo, este soluciona limitaciones de los otros modelos. Por ejemplo, las CNN evitan el problema de sobre ajuste que se podía producir en técnicas de recomendación basada en colaboración, por otra parte y tal como se menciona en el paper, los modelos de Deep learning son útiles para representar texto, audio, video, etc, por lo que son útiles para la representación por contenido.

Sin embargo, creo que hay una limitación de estas técnicas que es preocupante, su funcionamiento como caja negra por una parte que impide conocer que criterios está usando para recomendar y el nulo interés por parte de la industria/usuarios por saber como es que está funcionado realmente, considerando que ambos podrian salir sumanente perjudicados. Por ejemplo, que pasa si la CNN por muy trivial que pueda parecer, está simplemente recomendando por popularidad, haciendo a la industria gastar recursos en un software que no está haciendo más que ordenar los items (Aún si se diera el caso en que la recomendación _ideal_ fuera esa), o por otra parte, los usuarios dejan de explorar productos o alternativas por confiar plenamente en lo que el sistema recomienda, permitiendo que se pueda romper la competencia justa.