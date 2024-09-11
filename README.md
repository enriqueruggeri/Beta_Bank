# Beta_Bank
Beta Bank - Customer Loss Projection Model

En este proyecto vamos a trabajar con los datos de los clientes del banco Beta Bank. Cada mes los clientes del banco se están yendo poco a poco. Los banqueros descubrieron que es más barato salvar a los clientes existentes que atraer nuevos.

Por lo anterior, necesitamos predecir si un cliente dejará el banco pronto. Para ello disponemos de los datos sobre el comportamiento pasado de los clientes y la terminación de contratos con el banco.

Luego de cargar y preprocesar los datos para el análisis, en este proyecto exploramos dos técnicas para abordar el desequilibrio de clases en problemas de clasificación. Para ello ocupamos los métodos de ajuste de Pesos de Clases y de ajuste de Umbral.

Con el método de ajuste de Pesos de Clases, el utilizar diferentes pesos para las clases desequilibradas puede ayudar al modelo a dar más importancia a las muestras de la clase minoritaria durante el entrenamiento. En nuestro caso, encontramos que ajustar los pesos de las clases a 4.5 produjo el mejor F1-score en el conjunto de validación.

Con el método de Ajuste de Umbral, al modificar el umbral de probabilidad para asignar etiquetas de clase, podemos ajustar la sensibilidad y la especificidad del modelo para adaptarse a las necesidades específicas del problema. En nuestro caso, el F1-score alcanzó su punto máximo alrededor de un umbral de 0.36. Por lo que ese fue el valor que utilizamos en el modelo final.

Obtuvimos mejores resultados con el método de Ajuste de Umbral, en el conjunto de prueba el F1-score obtuvo a un valor de 0,6168, valor superior al valor límite de 0,59 solicitado para el proyecto.

También para ambos métodos fueron calculados los valores de AUC-ROC; obteniendo valores de 0,70 para el método de ajuste de Pesos de Clases y de 0,7511 para el método de ajuste de Umbral. Ambos representan valores razonables en el conjunto de prueba, lo que sugiere que el modelo generaliza bien a datos no vistos.

Tecnologías Utilizadas

  - pandas : librerías de pandas
  - pyplot de matplotlib : librerías pyplot de Matplotlib
  - numpy : la librerías de NumPy, se usa para funciones matemáticas complejas
  - stats de scipy : el módulo stats de la librería SciPy.
  - seaborn : la librería Seaborn para realizar unos gráficos
  - sns.set_theme() : librería para tener mejores gráficos
  - train_test_split de sklearn.model_selection : la función train_test_split de la biblioteca scikit-learn
  - DecisionTreeClassifier de sklearn : importamos la clase DecisionTreeClassifier
  - RandomForestClassifier de sklearn : importamos la clase RandomForestClassifier
  - accuracy_score de sklearn.metrics : importamos la función accuracy_score de la biblioteca scikit-learn
  - f1_score de sklearn.metrics : importamos la función f1_score de la biblioteca scikit-learn
    - - roc_auc_score de sklearn.metrics : importamos la función roc_auc_score de la biblioteca scikit-learn
shuffle de sklearn.utils : importamos la función shuffle de la biblioteca scikit-learn

Este proyecto nos ha permitido explorar y comprender el proceso de desarrollo de modelos de aprendizaje automático, desde la exploración de datos hasta la evaluación y selección de modelos.



Habilidades Relacionadas a Ciencia de Datos Desarrolladas

  - Exploración y Visualización de Datos: Análisis descriptivo y visualización para comprender los datos y sus características.
  - Preprocesamiento de Datos: Limpieza y transformación de datos, manejo de valores faltantes y codificación de variables categóricas.
  - Entrenamiento de Modelos: Implementación y evaluación de varios algoritmos de aprendizaje supervisado.
  - Evaluación de Modelos: Uso de métricas para evaluar y comparar el rendimiento de los modelos.
  - Optimización de Modelos: Ajuste de hiperparámetros y selección del modelo final.
