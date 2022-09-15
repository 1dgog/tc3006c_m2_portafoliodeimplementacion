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

![image](https://user-images.githubusercontent.com/71610960/190256081-83c0df57-3932-4e12-be87-11d091959c1a.png)

### Predicciones.

Se inserta tabla con predicciones (datos de prueba).

![image](https://user-images.githubusercontent.com/71610960/190315384-384d9adb-4c17-4844-8227-6c7b229a0b23.png)


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

Se presentan las predicciones realizadas con el subconjunto de prueba.

