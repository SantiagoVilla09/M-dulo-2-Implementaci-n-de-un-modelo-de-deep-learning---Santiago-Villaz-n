# M-dulo-2-Implementaci-n-de-un-modelo-de-deep-learning---Santiago-Villaz-n
“Clasificación binaria de cáncer de piel usando Keras/TensorFlow.”

Proyecto: Clasificación Binaria de Cáncer de Piel con Deep Learning

Autor: Santiago Villazón Ponce de León
Institución: Tecnológico de Monterrey
Módulo: Implementación de un Modelo de Deep Learning
Frameworks: TensorFlow y Keras
Modelo Base: EfficientNetV2-B0

Descripción del proyecto

Este proyecto implementa un modelo de deep learning para la detección binaria de cáncer de piel a partir de imágenes dermatológicas. Utiliza la arquitectura EfficientNetV2-B0 con la técnica de transfer learning, lo que permite aprovechar el conocimiento de modelos preentrenados para mejorar el desempeño con un conjunto de datos médico.

El objetivo principal es construir, entrenar y evaluar un modelo capaz de diferenciar entre imágenes de piel con cáncer (Cancer) y sin cáncer (Non-Cancer). A lo largo del notebook se incluyen las etapas completas del flujo de trabajo de aprendizaje profundo:

Preparación y análisis del conjunto de datos.

Preprocesamiento y técnicas de data augmentation.

Entrenamiento inicial del modelo.

Ajuste fino (fine-tuning) para optimizar la precisión.

Evaluación de resultados y generación de métricas.

Pruebas con imágenes externas para validar la capacidad de generalización.

Fuente del dataset

El conjunto de datos utilizado proviene de la plataforma Kaggle:
https://www.kaggle.com/datasets/kylegraupe/skin-cancer-binary-classification-dataset

Este dataset contiene imágenes clasificadas en dos carpetas principales: Cancer y Non_Cancer, distribuidas en conjuntos de entrenamiento y prueba.

Estructura del repositorio

/Skin_Data/ – Carpeta con el dataset de imágenes.

/runs/ – Modelos entrenados y logs del entrenamiento (.keras, .csv).

/reports/ – Figuras generadas durante la evaluación (matriz de confusión, curva ROC).

notebook.ipynb – Implementación completa del modelo y análisis de resultados.

requirements.txt – Dependencias necesarias para ejecutar el proyecto.

README.md – Descripción general del proyecto.

Requisitos de instalación

Para ejecutar el proyecto, se recomienda crear un entorno virtual con Python 3.12 y luego instalar las dependencias:

pip install -r requirements.txt

Uso del modelo entrenado

Una vez ejecutado el notebook, el modelo final se guarda en formato .keras.
Se puede realizar una predicción sobre una nueva imagen ejecutando:

pred = predict_image("ruta/a/imagen.jpg")
print(pred)

Resultados y conclusiones

El modelo logró un alto nivel de precisión y AUC al distinguir correctamente entre piel cancerosa y no cancerosa, demostrando la efectividad del uso de transfer learning con EfficientNetV2-B0. Las pruebas con imágenes nuevas, obtenidas de fuentes externas, confirmaron la capacidad de generalización del sistema.

Este proyecto evidencia el potencial de las redes convolucionales en el apoyo al diagnóstico médico, mostrando cómo la inteligencia artificial puede contribuir a la detección temprana del cáncer de piel.