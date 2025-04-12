**Etapas de un problema de Machine Learning**

* **Definir el problema:** Que se pretende predecir? o Que datos es necesario conseguir?
* **Explorar y entender** los datos para crear el modelo
* **Metrica de exito:** Definir una apropiada de cuantificar como de buenos son los resultados.
* **Preparar la estrategia para evaluar el modelo:** Separar las observaciones (filas) en conjunto de datos de entrenamiento, un conjunto de validacion (validacion cruzada) y un conjunto de test. Es muy importe asegurar que ninguna informacion del conjunto de test participa en el proceso de entrenamiento.
* **Preprocesamiento de Datos:** Aplicar las transformaciones necesarias para que los datos puedan ser interpretados por el algoritmo de machine learning seleccionado.
* **Ajustar un primer modelo capaz de superar unos resultados minimos:** Por ejemplo, en los problemas clasificacion, el minimo es superar el % de la clase mayoritaria (la moda). En los de regresion, la media de la variable respuesta.
* Gradualmente, mejorar el modelo incorporando-creando nuevas variables u optimizando los hiperparametros.
* **Evaluar la capacidad del modelo final** con el conjunto de test para tener una estimacion de la capacidad que tiene el modelo cuando predice nuevas observaciones
* **Entrenar el modelo final** con todos los datos disponibles.
  
# Analisis Exploratorio de los Datos

Antes de entrenar un modelo predictivo, o inclusive antes de realizar cualquier calculo con un nuevo conjunto de datos, es **muy importante** realizar una exploracion descriptiva de los mismos. Este proceso nos permite entender mejor que informacion contiene cada variable, asi como detectar posibles errores. Algunos frecuentes son:

* Que una columna se haya almacenado con el tipo de datos incorrecto: una variable numerica esta siendo reconocida como texto o viceversa.
* Que una variable contenga valores que no tienen sentido: por ejemplo, para que indicar en este caso que una vivienda tiene un valor de 0 o un espacio vacio.
*Que por error en una variable se haya introducido un texto.

# Division Train y Test

Evaluar la capacidad predictiva de un modelo, consiste en comprobar como son las proximas predicciones a los verdaderos valores de la variable respuesta.

Para poder cuantificarlo de forma correcta, se necesita disponer de un conjunto de observaciones, de las que conozca la variable respuesta, pero que el modelo no haya "visto", es decir, que no haya participado en su ajuste. Con esa finalidad se dividen los datos disponibles en un conjunto de entrenamiento y un conjunto de test.

El tamaño adecuado de las particiones depende en gran medida de la cantidad de datos disponibles y la seguridad en la estimacion del error, por lo cual se suele usar 80% y 20% - 70% y 30% que suelen buenos resultado. El reparto debe de hacerse de forma aleatoria o aleatoria estratificada.
