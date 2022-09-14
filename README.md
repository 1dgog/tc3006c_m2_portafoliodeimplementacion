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

### Predicciones.

Se inserta tabla con predicciones (datos de prueba).

### Matrices de confusion para entrenamiento, validación y prueba.

![cf_train](https://user-images.githubusercontent.com/71610960/190257712-8ee9470c-fee5-4ba5-958c-5f6146937c15.png)
![cf_valid](https://user-images.githubusercontent.com/71610960/190257707-61bb74cc-3b1b-4f65-b9bc-d7d3d54036de.png)
![cf_test](https://user-images.githubusercontent.com/71610960/190257713-b6627f37-2dce-4b3b-bc57-c5c01c5b607b.png)


## Con Framework


