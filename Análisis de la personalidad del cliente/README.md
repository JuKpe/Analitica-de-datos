#  Análisis de la personalidad del cliente

## OBJETIVO
Aplicar técnicas de limpieza, modelado predictivo y segmentación en Python, y construir un tablero de visualización interactiva en Power BI que ayude a comprender el comportamiento del cliente y su respuesta a campañas de marketing.

## 📚 DATASET BASE
Customer Personality Analysis (Kaggle)

## Descripción:
Este dataset contiene información sobre los clientes de una compañía de productos de consumo, incluyendo:
* Datos demográficos: edad, estado civil, ingresos, etc.
* Información sobre campañas de marketing.
* Historial de compras por categoría de producto.
* Nivel de participación en campañas promocionales.
* Respuesta a campañas de marketing.

# 🧠 PARTE 1: ANÁLISIS Y MODELADO CON PYTHON (SKLEARN)
A. Preprocesamiento de datos
  1. Carga el dataset en un Jupyter Notebook.
  2. Limpia los datos:
     * Elimina columnas irrelevantes.
     * Trata valores nulos si los hubiera.
     * Convierte fechas (Dt_Customer) a año de registro.
     * Codifica variables categóricas (estado civil, educación, etc.).
     * Normaliza o estandariza las variables numéricas si es necesario.

B. Modelado predictivo
  1. Define el problema: ¿Se puede predecir si un cliente responderá a una campaña? (Response: 0 o 1).
  2. Aplica el siguiente flujo:
     * División train_test_split.
     * Comparación entre al menos 2 modelos: LogisticRegression, RandomForestClassifier.
     * Evaluación: matriz de confusión, accuracy, precision, recall, F1-score.
  3. Interpreta resultados y exporta el archivo con las predicciones.

C. Segmentación con KMeans
  1. Aplica KMeans con entre 3 y 5 clústeres.
  2. Usar columnas como ingresos, gasto en productos, edad, etc.
  3. Visualiza los clústeres (gráfico 2D con PCA o t-SNE).
  4. Interpreta las características de cada clúster (perfiles).

# 📊 PARTE 2: VISUALIZACIÓN INTERACTIVA EN POWER BI (20 pts)
A. Dataset base: clientes_resultado.csv
  1. Crea un dashboard en Power BI que contenga:
     * Gráfico de barras: gasto por tipo de producto y clúster.
     * Filtro de respuesta (Respuesta_predicha) y año de registro.
     * Tarjetas: promedio de ingreso, edad, tasa de respuesta por clúster.
     * Gráfico de dispersión: ingreso vs gasto con color por clúster.
     * Visualización de distribución de campañas exitosas.
  2. Exporta como dashboard.pbix.
