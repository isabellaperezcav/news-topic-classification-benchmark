# Benchmark de Clasificación de Temas de Noticias

Este repositorio contiene un proyecto de benchmark para la clasificación de temas de noticias utilizando el dataset **AG News Classification**. El objetivo es desarrollar y comparar diferentes modelos de aprendizaje automático para clasificar noticias en cuatro categorías: World, Sports, Business y Sci/Tech.

## Descripción del Proyecto

El proyecto incluye un análisis exploratorio de datos (EDA) para entender la estructura y características del dataset, seguido de la implementación de varios modelos de clasificación. Se utiliza el dataset AG News, disponible en [Kaggle](https://www.kaggle.com/datasets/amananandrai/ag-news-classification-dataset), que contiene noticias divididas en archivos de entrenamiento (`train.csv`) y validación (`test.csv`), con las columnas `Class Index`, `Title` y `Description`.

### Objetivos
- Realizar un EDA para analizar la distribución de clases, longitud de los textos y palabras más frecuentes por categoría.
- Preprocesar el texto usando técnicas como limpieza y vectorización con TF-IDF.
- Comparar el rendimiento de diferentes modelos de clasificación, incluyendo Logistic Regression, Random Forest, SVM, XGBoost y LightGBM.

## Estructura del Repositorio

- `README.md`: Este archivo con información general del proyecto.
- `train.csv`: Dataset de entrenamiento.
- `test.csv`: Dataset de validación.
- `EDA_modelo.ipynb`: scripts de Python utilizados para analisis y preparacion de los datos y para entrenar los modelos.


## Instrucciones de Uso

1. **Clonar el repositorio**:
   ```bash
   git clone https://github.com/isabellaperezcav/news-topic-classification-benchmark.git
   cd news-topic-classification-benchmark
   ```

2. **Instalar dependencias**:
   Ejecuta el comando 
```bash
pip install -r requirements.txt
```

3. **Ejecutar el código**:
   - Para el EDA y para comparar todos los modelos, ejecuta el script `EDA_modelo.ipynb` que incluye Logistic Regression, Random Forest, SVM, XGBoost y LightGBM.


4. **Explorar resultados**:
   Los resultados incluyen reportes de clasificación (precisión, recall, F1-score) y visualizaciones como histogramas y gráficos de barras.

## Metodología

### Análisis Exploratorio de Datos (EDA)
- Se analizó la distribución de clases usando gráficos de barras.
- Se calculó la longitud de los textos (título + descripción) y se visualizó con histogramas.
- Se identificaron las palabras más frecuentes por categoría tras preprocesamiento (eliminación de stop words y lematización).

### Preprocesamiento
- Combinación de `Title` y `Description` en una sola columna `Text`.
- Limpieza del texto: conversión a minúsculas y eliminación de caracteres especiales.
- Vectorización con TF-IDF para convertir el texto en representaciones numéricas.

### Modelos de Clasificación
Se probaron los siguientes modelos:
- **Logistic Regression**: Modelo baseline rápido y efectivo.
- **Random Forest**: Ensemble de árboles para reducir el sobreajuste.
- **SVM (LinearSVC)**: Optimizado para datos sparse como TF-IDF.
- **XGBoost**: Modelo de boosting robusto.
- **LightGBM**: Versión eficiente de boosting.

### Evaluación
- Se evaluó cada modelo con métricas como precisión, recall y F1-score (promedio ponderado).
- Se midió el tiempo de entrenamiento para comparar eficiencia.
- Se generaron visualizaciones para comparar los F1-scores.

## Resultados Esperados
- Logistic Regression y SVM suelen ofrecer los mejores F1-scores (~0.85-0.90) debido a su idoneidad para datos de texto.
- Random Forest puede tener un rendimiento decente (~0.80-0.85) pero con mayor tiempo de entrenamiento.
- XGBoost y LightGBM también alcanzan F1-scores altos (~0.85-0.90), con LightGBM siendo más rápido.

## Contribuciones
Este proyecto fue desarrollado por Isabella Pérez. Si deseas contribuir, por favor abre un issue o envía un pull request con tus sugerencias o mejoras.


## Contacto
Para preguntas o comentarios, contacta a Isabella Pérez en [isabellaperezcav@gmail.com].

```

---