# Portafolio de implementacion para aprendizaje de máquina (módulo 2)
Javier de Golferichs García A01139500

Se incluye en el README.md secciones para [Sin Framework](##-Sin-Framework) y  [Con Framework](##-Con-Framework) (más abajo)

Se incluyen .ipynb y .py de ambas entregas (sin y con framework).

## Sin Framework

Se usa archivo utilizado es **wines.data**. Se hace una **regresión logística de orden 2** que toma en cuenta **dos características** (alcohol, flavanoids).

Se hicieron columnas dummy binarias con base en la clase (1, 2 o 3), para hacer la clasificación.

Se hizo una vizualización de los datos.

Para hacer la separación en subconjuntos (entrenamiento, validación y prueba), se utilizó sklearn.model_selection.train_test_split.

### Función de clasificación

Se utilizó un $\alpha = 0.05$ y 10000 iteraciones en la función de clasificación.
La salida de la función de clasificación es:

| |theta inicial| | |J entrenamiento|J validacion|theta refinada |||
|:----|:----|:----|:----|:----|:----|:----|:----|:----|
| |0|1|2| | |0|1|2|
|Clase 1|2|1|0.5|-0.145830812|-0.255904113|-4.528507542|-0.218032685|2.888516617|
|Clase 2|2|1|0.5|-0.239314728|-0.232469886|10.12620338|-0.87245963|0.335677986|
|Clase 3|2|1|0.5|-0.068253754|-0.053346059|0.464055325|0.507980433|-5.732727431|

### Predicciones de subconjunto de prueba

Se inserta tabla con predicciones (datos de prueba). Los vectores theta descritos en la tabla corresponden a los de la clase en forma `np.array(1/(1+np.exp(-(theta1[0]+theta1[1]*x_test1_a+theta1[2]*x_test1_b))))`, donde `x_test1_a` y `x_test1_b`, son las entradas de ambas características (alcohol, flavanoids). 


|    |   **Real** |   **Prediccion** |   alcohol |   flavanoids |          1 |        2 |           3 |
|---:|-------:|-------------:|----------:|-------------:|-----------:|---------:|------------:|
|  0 |      2 |            1 |     12.43 |         3.15 | 0.865317   | 0.583927 | 1.26247e-05 |
|  1 |      1 |            1 |     13.05 |         3    | 0.784437   | 0.437243 | 4.08737e-05 |
|  2 |      2 |            2 |     12.6  |         1.36 | 0.0339825  | 0.398848 | 0.282539    |
|  3 |      2 |            2 |     11.76 |         2.03 | 0.226377   | 0.633556 | 0.00548886  |
|  4 |      3 |            3 |     13.88 |         0.34 | 0.00139606 | 0.13361  | 0.996188    |
|  5 |      2 |            1 |     12.37 |         3.1  | 0.849263   | 0.592541 | 1.63106e-05 |
|  6 |      1 |            1 |     14.83 |         2.98 | 0.699695   | 0.14039  | 0.000113213 |
|  7 |      3 |            3 |     12.6  |         0.66 | 0.00463581 | 0.344063 | 0.956103    |
|  8 |      1 |            1 |     13.5  |         2.61 | 0.516764   | 0.315208 | 0.000480296 |
|  9 |      1 |            1 |     13.24 |         2.69 | 0.587793   | 0.372341 | 0.000266114 |
| 10 |      2 |            1 |     13.05 |         2.65 | 0.569726   | 0.408578 | 0.000303894 |
| 11 |      3 |            3 |     13.36 |         0.5  | 0.00247962 | 0.203912 | 0.987682    |
| 12 |      1 |            1 |     13.39 |         2.94 | 0.739674   | 0.361436 | 6.85208e-05 |
| 13 |      1 |            1 |     13.73 |         3.25 | 0.865946   | 0.318274 | 1.37737e-05 |
| 14 |      1 |            1 |     14.21 |         2.65 | 0.506954   | 0.200704 | 0.000547681 |

### Matrices de confusion para subconjuntos de entrenamiento, validación y prueba

Las matrices de confusión corresponden a matrices de multicaso, tal que en la diagonal principal se ubican las predicciones del modelo con las categorías originales.

![cf_train](https://user-images.githubusercontent.com/71610960/190315590-d8b68395-291b-4cd7-ab81-10fe80ce6637.png)
![cf_valid](https://user-images.githubusercontent.com/71610960/190315600-264f88fa-bf15-4be2-b12f-21c3eebdc624.png)
![cf_test](https://user-images.githubusercontent.com/71610960/190315605-5d502872-7716-40a3-b954-0adbdefb6e29.png)



## Con Framework

El archivo utilizado es **wine.data**.

Se hace una implementación de **redes neuronales**, en la que se varía el **de 5 a 35 número de capas ocultas**, y dentro de ese ciclo se itera de **5 a 35 neuronas**. 

Se usa **sklearn.neural_network.MLPClassifier** como método de framework.

Se inicia por importar la base de datos. Se usan todas las carácterísticas para hacer el modelo (13 características).

Se separa el dataset en subconjuntos de entrenamiento (113, 13), validación (33, 13) y prueba (12, 13).

### Puntajes para subconjuntos de entrenamiento, validación y prueba, variando parámetros

Se presentan los resultados de los puntajes obtenidos variando el número de capas ocultas (5 a 35), y el número de partículas por capa (5 a 35).

![image](https://user-images.githubusercontent.com/71610960/190313681-3d52b731-28ae-4830-8d9c-39b0591eac6b.png)
![image](https://user-images.githubusercontent.com/71610960/190313732-027bd69d-d4c1-47a8-855e-8e3be8b8007f.png)
![image](https://user-images.githubusercontent.com/71610960/190313752-faa42d37-3eb4-4e74-982f-4cfe1159db89.png)

### Predicciones de datos de prueba

Se presentan las predicciones realizadas con el subconjunto de prueba, del modelo con 35 capas ocultas y 5 neuronas por capa (seleccionado como modelo refinado en reporte de análisis por no tener underfitting ni overfitting, y ser el más simple de los de 35 capas ocultas). 
%% recuerda hacer el cambio a no la ultima de abajo derecha, sino arriba derecha para el valor obtenido

|    |   index |   0 |   alcohol |   malic_acid |   ash |   alcalinity_of_ash |   magnesium |   total_phenols |   flavanoids |   nonflavanoid_phenols |   proanthocyanins |   color_intensity |   hue |   od280 |   proline |
|---:|--------:|----:|----------:|-------------:|------:|--------------------:|------------:|----------------:|-------------:|-----------------------:|------------------:|------------------:|------:|--------:|----------:|
|  0 |       1 |   1 |     13.39 |         1.77 |  2.62 |                16.1 |          93 |            2.85 |         2.94 |                   0.34 |              1.45 |              4.8  |  0.92 |    3.22 |      1195 |
|  1 |       2 |   2 |     12.69 |         1.53 |  2.26 |                20.7 |          80 |            1.38 |         1.46 |                   0.58 |              1.62 |              3.05 |  0.96 |    2.06 |       495 |
|  2 |       2 |   2 |     12.16 |         1.61 |  2.31 |                22.8 |          90 |            1.78 |         1.69 |                   0.43 |              1.56 |              2.45 |  1.33 |    2.26 |       495 |
|  3 |       2 |   2 |     13.05 |         5.8  |  2.13 |                21.5 |          86 |            2.62 |         2.65 |                   0.3  |              2.01 |              2.6  |  0.73 |    3.1  |       380 |
|  4 |       3 |   1 |     13.36 |         2.56 |  2.35 |                20   |          89 |            1.4  |         0.5  |                   0.37 |              0.64 |              5.6  |  0.7  |    2.47 |       780 |
|  5 |       2 |   2 |     12.52 |         2.43 |  2.17 |                21   |          88 |            2.55 |         2.27 |                   0.26 |              1.22 |              2    |  0.9  |    2.78 |       325 |
|  6 |       2 |   2 |     11.76 |         2.68 |  2.92 |                20   |         103 |            1.75 |         2.03 |                   0.6  |              1.05 |              3.8  |  1.23 |    2.5  |       607 |
|  7 |       3 |   2 |     13.88 |         5.04 |  2.23 |                20   |          80 |            0.98 |         0.34 |                   0.4  |              0.68 |              4.9  |  0.58 |    1.33 |       415 |
|  8 |       2 |   2 |     11.62 |         1.99 |  2.28 |                18   |          98 |            3.02 |         2.26 |                   0.17 |              1.35 |              3.25 |  1.16 |    2.96 |       345 |
|  9 |       1 |   3 |     14.22 |         1.7  |  2.3  |                16.3 |         118 |            3.2  |         3    |                   0.26 |              2.03 |              6.38 |  0.94 |    3.31 |       970 |
| 10 |       3 |   2 |     13.78 |         2.76 |  2.3  |                22   |          90 |            1.35 |         0.68 |                   0.41 |              1.03 |              9.58 |  0.7  |    1.68 |       615 |
| 11 |       2 |   2 |     13.11 |         1.01 |  1.7  |                15   |          78 |            2.98 |         3.18 |                   0.26 |              2.28 |              5.3  |  1.12 |    3.18 |       502 |

### Matriz de confusión para modelo simple (5 capas ocultas, 5 neuronas por capa) y modelo refinado (35 capas ocultas, 5 neuronas por capa)

![cf_test_con_framework_ini](https://user-images.githubusercontent.com/71610960/190330198-3cf1dc1f-2e61-4645-bad3-542cc5410910.png)
![cf_test_con_framework_ref](https://user-images.githubusercontent.com/71610960/190330194-6cf4fc8f-5fe7-44bb-8ee0-91324447706e.png)
