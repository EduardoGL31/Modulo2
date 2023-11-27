# Helado vs Pizza
Dataset from:
https://www.kaggle.com/datasets/hemendrasr/pizza-vs-ice-cream

Con este modelo de Deep Learning, puedes realizar la clasificación de imágenes para determinar si se trata de una pizza o un helado.

[Code](Pizza_or_ice_cream.ipynb)


Preparación de datos:

Las imágenes se cargan utilizando ImageDataGenerator desde directorios que contienen conjuntos de entrenamiento, validación y prueba.
Se aplica aumento de datos al conjunto de entrenamiento (rotación, desplazamiento en ancho y alto, cizallamiento, zoom, volteo horizontal).
Modelo 1:

Dos capas convolucionales con max-pooling entre ellas.
Capa de aplanamiento seguida de dos capas densas para la clasificación.
Compilación utilizando el optimizador Adam, pérdida de entropía cruzada binaria y métrica de precisión.
Entrenamiento del modelo con 20 épocas.

Modelo 2:

Arquitectura similar al Modelo 1, pero con características adicionales.
Se añaden capas de dropout para reducir el sobreajuste.
Se agrega una capa convolucional y una capa de max-pooling adicionales.
La última capa densa utiliza la función de activación sigmoide para clasificación binaria.
Compilación y entrenamiento similares al Modelo 1.
Análisis de resultados:

Se generan gráficos para la precisión/pérdida de entrenamiento y validación para ambos modelos.
Se realiza la evaluación del modelo en el conjunto de prueba.

Mejoras en el Modelo 2:

Se añaden capas de dropout para mitigar el sobreajuste.
Se incorporan capas adicionales de convolución y max-pooling para aumentar la complejidad del modelo.
Se utiliza la activación sigmoide en la capa final para la clasificación binaria.
Resultados:

El Modelo 1 muestra resultados menos satisfactorios, con menor precisión en los conjuntos de entrenamiento, validación y prueba.
El Modelo 2 demuestra un rendimiento mejorado, logrando mayor precisión en todos los conjuntos.
Guardado del Modelo:

El Modelo 2 entrenado se guarda como 'Pizza-Ice_model.h5'.
Ejemplos de Predicciones:

Se cargan dos imágenes de muestra ('pizza.jpg' e 'icecream.jpg'), se preprocesan y se clasifican utilizando el modelo entrenado.
Las predicciones se muestran junto con las imágenes correspondientes.
