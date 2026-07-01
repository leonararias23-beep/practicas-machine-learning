# Práctica de Machine Learning

En este repositorio se reúne tres algoritmos de Machine Learning. Cada notebook aborda un problema distinto (predicción numérica y clasificación) y documenta, dentro de sus propias celdas, el sustento teórico de cada modelo, la implementación en Python y el análisis de los resultados obtenidos.

**Autor:** Nelson Leonardo Páez Arias

## Estructura del repositorio


├── data/
│   ├── china_gdp.csv
│   ├── dataset_flor_iris.csv
│   └── alturas-pesos.csv
├── Regresion_No_lineal_PIB_China.ipynb
├── Clasificacion_Hoja_iris_ml.ipynb
├── Regresion_lineal_prediccion_peso.ipynb
└── README.md


Todos los conjuntos de datos utilizados por los notebooks se encuentran en la carpeta `data/`. La explicación teórica de cada técnica, así como el análisis y las conclusiones de los resultados, está desarrollada directamente en las celdas de tipo Markdown dentro de cada notebook, por lo que este documento se limita a describir el contenido general del repositorio y la forma de ejecutarlo.

## Proyectos

### 1. Regresión No Lineal. Predicción del PIB de China

**Archivo:** `Regresion_No_lineal_PIB_China.ipynb`
**Dataset:** `data/china_gdp.csv`

Proyecto de regresión que compara tres modelos no lineales para predecir el Producto Interno Bruto (PIB) de China y proyectar su valor para los años 2025 y 2026:

- Regresión Polinomial (grado 3)
- Regresión con Splines (grado 1)
- Regresión con Funciones de Base Radial (RBF, mediante SVR)

Cada modelo se evalúa con las métricas MAE, MSE, RMSE y R², y adicionalmente se calcula el error porcentual de la predicción frente al valor real del PIB en 2025 que es de 19.652 billones de USD. El notebook cierra con una comparación conjunta de los tres modelos para determinar cuál generaliza mejor fuera del rango de datos históricos.

### 2. Clasificación de Especies. Dataset Iris

**Archivo:** `Clasificacion_Hoja_iris_ml.ipynb`
**Dataset:** `data/dataset_flor_iris.csv`

Proyecto de clasificación multiclase que utiliza el conjunto de datos Iris (150 muestras, 3 especies) para comparar el desempeño de tres algoritmos:

- Regresión Logística
- Random Forest
- Árbol de Decisión

El notebook incluye un análisis exploratorio de datos (EDA) mediante `pairplot`, la preparación y escalamiento de los datos, y la evaluación de cada modelo con Accuracy, Precision, Recall y F1-Score, además de matrices de confusión. Finaliza con una tabla comparativa de las tres técnicas.

### 3. Regresión Lineal. Predicción de Peso Corporal

**Archivo:** `Regresion_lineal_prediccion_peso.ipynb`
**Dataset:** `data/alturas-pesos.csv`

Proyecto de regresión lineal multivariable que estima el peso corporal de una persona a partir de la altura y el sexo. Incluye la codificación de la variable categórica sexo, la división de los datos mediante la técnica Hold-Out (70/30), el entrenamiento del modelo y la evaluación de sus resultados con MSE, RMSE y R².

## Tecnologías utilizadas

- Python 3
- pandas
- NumPy
- scikit-learn
- Matplotlib
- Seaborn

## Requisitos

```
pip install pandas numpy scikit-learn matplotlib seaborn
```

## Instrucciones de uso

Los notebooks fueron desarrollados y ejecutados en Google Colab, por lo que las rutas de carga de los archivos CSV apuntan a `/content/`.

1. Clonar el repositorio o descargar el notebook deseado junto con su dataset correspondiente desde la carpeta `data/`.
2. Abrir el notebook en Google Colab.
3. Subir el archivo CSV correspondiente al entorno de Colab (por ejemplo, arrastrándolo a la sección de archivos o mediante `files.upload()`), de modo que quede disponible en la ruta `/content/`.
4. Ejecutar las celdas en orden.

Si se desea ejecutar algún notebook en un entorno local, basta con actualizar la ruta del archivo CSV para que apunte a la ubicación correspondiente dentro de `data/` (por ejemplo, `data/china_gdp.csv`).

