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

![cf_train](https://user-images.githubusercontent.com/71610960/190257430-519ecbb0-2954-4477-afcb-fbd44dfe6d2a.png)
![cf_valid](https://user-images.githubusercontent.com/71610960/190257427-3d127cde-c2f7-43eb-b364-e6451192ae74.png)
![cf_test](https://user-images.githubusercontent.com/71610960/190257428-a1af4d71-79e2-4303-bc0a-30908a9270ec.png)

## Con Framework


