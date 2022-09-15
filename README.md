# Portafolio de implementacion
Javier de Golferichs García A01139500

Se incluye en el README.md secciones para [Sin Framework](##-Sin-Framework) y  [Con Framework](##-Con-Framework) (más abajo)

## Sin Framework

Se usa el dataset de wines.data. Se hace una regresión logística de orden 2 que toma en cuenta dos características (alcohol, flavanoids).

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

### Predicciones.

Se inserta tabla con predicciones (datos de prueba).

|index|alcohol|flavanoids|1|2|3|Real|Prediccion|
|---|---|---|---|---|---|---|---|
|0|12\.43|3\.15|0\.8653171726479987|0\.5839271426938165|1\.2624743120118493e-05|2|1|
|1|13\.05|3\.0|0\.784437459263086|0\.4372425034925187|4\.087372194117752e-05|1|1|
|2|12\.6|1\.36|0\.03398248321814226|0\.39884836632327053|0\.2825392973610589|2|2|
|3|11\.76|2\.03|0\.22637695406560562|0\.6335564096093226|0\.005488855873863599|2|2|
|4|13\.88|0\.34|0\.0013960581861285173|0\.13361049527386706|0\.9961876749037951|3|3|
|5|12\.37|3\.1|0\.8492626592513574|0\.5925409421582374|1\.6310555709680198e-05|2|1|
|6|14\.83|2\.98|0\.6996952849477759|0\.14039024146459814|0\.00011321342280222218|1|1|
|7|12\.6|0\.66|0\.0046358069651868125|0\.34406288333815715|0\.9561025385351241|3|3|
|8|13\.5|2\.61|0\.5167636095429146|0\.3152080700182921|0\.00048029606566297913|1|1|
|9|13\.24|2\.69|0\.5877930515119177|0\.3723406698302508|0\.00026611375626761055|1|1|
|10|13\.05|2\.65|0\.5697263981978795|0\.40857772000191106|0\.00030389398181477885|2|1|
|11|13\.36|0\.5|0\.002479623340815851|0\.20391247451893504|0\.987682133994519|3|3|
|12|13\.39|2\.94|0\.7396737693235036|0\.3614358002094786|6\.852075593132947e-05|1|1|
|13|13\.73|3\.25|0\.8659463308531189|0\.31827427917417533|1\.3773676883749057e-05|1|1|
|14|14\.21|2\.65|0\.5069538111435282|0\.2007038165824665|0\.0005476806206184886|1|1|

### Matrices de confusion para entrenamiento, validación y prueba.

![cf_train](https://user-images.githubusercontent.com/71610960/190315590-d8b68395-291b-4cd7-ab81-10fe80ce6637.png)
![cf_valid](https://user-images.githubusercontent.com/71610960/190315600-264f88fa-bf15-4be2-b12f-21c3eebdc624.png)
![cf_test](https://user-images.githubusercontent.com/71610960/190315605-5d502872-7716-40a3-b954-0adbdefb6e29.png)



## Con Framework

Se hace una implementación de **redes neuronales**, en la que se varía el **de 5 a 35 número de capas ocultas**, y dentro de ese ciclo se itera de **5 a 35 neuronas**. 

Se usa sklearn.neural_network.MLPClassifier como método de framework.

Se inicia por importar la base de datos. Se usan todas las carácterísticas para hacer el modelo (13 características).

Se separa el dataset en subconjuntos de entrenamiento (113, 13), validación (33, 13) y prueba (12, 13).

### Puntajes

Se presentan los resultados de los puntajes obtenidos variando el número de capas ocultas (5 a 35), y el número de partículas por capa (5 a 35).

![image](https://user-images.githubusercontent.com/71610960/190313681-3d52b731-28ae-4830-8d9c-39b0591eac6b.png)
![image](https://user-images.githubusercontent.com/71610960/190313732-027bd69d-d4c1-47a8-855e-8e3be8b8007f.png)
![image](https://user-images.githubusercontent.com/71610960/190313752-faa42d37-3eb4-4e74-982f-4cfe1159db89.png)

### Predicciones

Se presentan las predicciones realizadas con el subconjunto de prueba, del modelo con 35 capas ocultas y 5 neuronas por capa (seleccionado como modelo refinado en reporte de análisis por no tener underfitting ni overfitting, y ser el más simple de los de 35 capas ocultas).




