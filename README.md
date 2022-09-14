# tc3006c_portafoliodeimplementacion
Javier de Golferichs García A01139500

Se incluye en el README.md [Sin Framework](##-Sin-Framework) y  [Con Framework](##-Con-Framework)

## Sin Framework

Se usa el dataset de wines.data. Se hace una regresión logística de orden 2 que toma en cuenta dos características (alcohol, flavanoids).

Se hicieron columnas dummy binarias con base en la clase (1, 2 o 3), para hacer la clasificación.

Se hizo una vizualización de los datos.

Para hacer la separación en subconjuntos (entrenamiento, validación y prueba), se utilizó sklearn.model_selection.train_test_split.

### Función de clasificación
Se utilizó un $\alpha = 0.05$ y 10000 iteraciones en la función de clasificación.
La salida de la función de clasificación es:

![image](https://user-images.githubusercontent.com/71610960/190256081-83c0df57-3932-4e12-be87-11d091959c1a.png)

### Predicciones

Se inserta tabla con predicciones (datos de prueba).

### Matrices de confusion para entrenamiento, validación y prueba.

![cf_valid](https://user-images.githubusercontent.com/71610960/190256913-25028e32-bd33-4338-8f14-81332df4cdc8.png)
![cf_test](https://user-images.githubusercontent.com/71610960/190256915-7a3a9e44-5853-4197-b1ef-8abf9d6a9cb6.png)
![cf_train](https://user-images.githubusercontent.com/71610960/190256918-e86a00da-dd4e-4a28-80ef-3cc1b52ebcfc.png)

## Con Framework


