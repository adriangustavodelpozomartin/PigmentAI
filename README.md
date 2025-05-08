# PigmentAI
*Visión inteligente del arte*

![Portada de PigmentAI](./pigmentAI)

PigmentAI es un proyecto que une arte e inteligencia artificial a través de un pipeline completo para el tratamiento y generación de imágenes artísticas. Desde la exploración de datos hasta la síntesis de nuevas obras, este repositorio ilustra cómo la IA puede analizar y crear arte digital de forma profesional.

---

## Índice

- [Descripción del Proyecto](#descripción-del-proyecto)
  - [1. Exploratory Data Analysis (EDA)](#1-exploratory-data-analysis-eda)
  - [2. Reconocimiento de Objetos y Rostros](#2-reconocimiento-de-objetos-y-rostros)
  - [3. CNN desde cero (From Scratch)](#3-cnn-desde-cero-from-scratch)
  - [4. Transfer Learning](#4-transfer-learning)
  - [5. Generación de Imágenes (Neural Style Transfer)](#5-generación-de-imágenes-neural-style-transfer)
- [Archivos auxiliares](#archivos-auxiliares)
- [Estructura del Proyecto](#estructura-del-proyecto)
- [Fuente de Datos](#fuente-de-datos)
- [Requisitos](#requisitos)
- [Autores](#autores)

---

## Descripción del Proyecto

PigmentAI nace con la misión de explorar la intersección entre arte y inteligencia artificial mediante un pipeline que abarca:
- **Analizar** colecciones de arte digital para extraer información y patrones.
- **Detectar** objetos y rostros en obras pictóricas usando técnicas clásicas y redes neuronales.
- **Clasificar** imágenes mediante CNN implementadas desde cero y con modelos preentrenados.
- **Generar** nuevas obras combinando estilo y contenido con algoritmos de transferencia de estilo.

---

### 1. Exploratory Data Analysis (EDA)

En el notebook **`01_Exploratory_Data_Analysis.ipynb`** se realiza:
- Selección y preprocesamiento de imágenes de obras de arte.
- Análisis de distribuciones de píxeles (histogramas en escala de grises y canales RGB).
- Estadísticas y visualizaciones para entender la naturaleza del dataset.

---

### 2. Reconocimiento de Objetos y Rostros

El notebook **`02_Reconocimiento_Objetos_Rostros.ipynb`** incluye:
- Detección y clasificación con HOG+SVM y modelos DNN preentrenados (SSD+ResNet10).
- Evaluación comparativa de arquitecturas y ajuste de hiperparámetros.
- Pipeline completo: carga de datos, entrenamiento, métricas y conclusiones.

---

### 3. CNN desde cero (From Scratch)

En **`03_CNN_from_scratch.ipynb`** encontrarás:
- Definición de una CNN propia con sus capas y funciones auxiliares.
- Implementación de bucles de entrenamiento y validación.
- Establecimiento de una línea base y optimización de hiperparámetros para mejorar precisión.

---

### 4. Transfer Learning

El notebook **`04_transfer_learning.ipynb`** aborda:
- Adaptación de modelos preentrenados (VGG-16, ResNet-50) al dominio artístico.
- Aplicación de técnicas de data augmentation para robustecer el entrenamiento.
- Comparativa de resultados y optimización de métricas de pérdida y precisión.

---

### 5. Generación de Imágenes (Neural Style Transfer)

En **`05_Style_transfer.ipynb`** se implementa:
- Algoritmo de transferencia de estilo (Gatys et al.).
- Cálculo de pérdidas de contenido y estilo.
- Generación de nuevas obras fusionando la estructura de una imagen con el estilo de otra.

---

## Archivos auxiliares

- **class_weights.json**: Diccionario con los pesos de cada clase para balancear el entrenamiento en las tareas de clasificación.
- **Pesos de modelos preentrenados**: Por restricciones de espacio, los archivos con los pesos entrenados no se incluyen en el repositorio, pero pueden generarse ejecutando el notebook correspondiente (por ejemplo, `03_CNN_from_scratch.ipynb`, `04_transfer_learning.ipynb` o `05_Style_transfer.ipynb`).

---

## Fuente de Datos

Los datos utilizados en este proyecto provienen del dataset de Kaggle: [Best Artworks of All Time](https://www.kaggle.com/ikarus777/best-artworks-of-all-time).

---

## Estructura del Proyecto

```plaintext
PigmentAI/
├── 01_Exploratory_Data_Analysis.ipynb
├── 02_Reconocimiento_Objetos_Rostros.ipynb
├── 03_CNN_from_scratch.ipynb
├── 04_transfer_learning.ipynb
├── 05_Style_transfer.ipynb
├── class_weights.json
├── requirements.txt
├── pigmentAI        # Logo del proyecto
└── README.md
```

---

## Requisitos

Para instalar las dependencias necesarias, ejecuta:

```bash
pip install -r requirements.txt
```

---

## Autores

- **Adrián Gustavo del Pozo Martín**  
- **Alberto Sáez-Royuela Ariza**  
- **Guillaume Guers Victor**
