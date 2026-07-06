# Clasificaci-n-de-Vinos-utilizando-LDA-y-QDA
Esta tarea contiene un cuaderno en Python (Google Colab) donde se implementan y comparan los modelos de Análisis Discriminante Lineal (LDA) y Cuadrático (QDA) utilizando el Wine Dataset de UCI. Se evalúa el impacto de la matriz de covarianza y la forma de las fronteras de decisión (lineal vs cuadrática).


Instrucciones para ejecutar esta Tarea:

1. Es necesario contar con Python 3.x y las siguientes librerías instaladas: pandas, numpy, matplotlib, seaborn y scikit-learn.

2. No es necesario descargar el dataset manualmente, ya que el código lo importa directamente a través del comando load_wine() de scikit-learn.

3. Abra el archivo .ipynb en Google Colab o Jupyter Notebook.

4. Ejecute las celdas en orden secuencial para cargar los datos, visualizar los gráficos exploratorios y entrenar los modelos.



Principales hallazgos:

Alto desempeño general: Ambos modelos demostraron una excelente capacidad predictiva utilizando los datos en bruto (sin estandarización previa). El modelo LDA logró una exactitud del 98.15%, cometiendo un único error en el conjunto de prueba.

Superioridad predictiva del QDA: El modelo QDA superó al LDA al alcanzar una exactitud perfecta del 100%. Al no asumir una matriz de covarianza compartida, el QDA logró adaptarse de manera óptima a la varianza y dispersión individual de cada clase de vino.

Flexibilidad topológica en fronteras: La visualización bidimensional de las fronteras de decisión evidenció que mientras el LDA traza separaciones estrictamente rectas y rígidas, el QDA genera fronteras curvas que "abrazan" la distribución natural de los datos, demostrando su capacidad para modelar estructuras complejas.

Robustez computacional ante datos no escalados: A pesar de la gran diferencia de escalas entre las variables químicas analizadas (por ejemplo, los valores de la Prolina frente a los Flavanoides), el uso del solucionador svd (Descomposición en Valores Singulares) permitió a ambos modelos procesar los datos de manera estable y sin colapso matemático.
