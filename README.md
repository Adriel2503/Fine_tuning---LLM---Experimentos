# Proyectos de Procesamiento de Lenguaje Natural (NLP) con Transformers

Este repositorio contiene una colección de proyectos de NLP utilizando modelos preentrenados de `Hugging Face Transformers` para abordar diferentes tareas. A continuación, se describe cada proyecto y las técnicas empleadas.

## Proyectos

### 1. Análisis de Sentimientos (Sentiment Analysis)
   - **Descripción**: Realiza análisis de sentimientos sobre textos usando modelos de `Hugging Face`, como `distilbert-base-uncased` y `bert-base-multilingual-uncased-sentiment`.
   - **Técnicas Utilizadas**:
     - Uso de modelos preentrenados para clasificar sentimientos en positivo y negativo.
     - **Fine-tuning** de un modelo BERT en un dataset de reseñas de productos, adaptando el modelo a la tarea específica.
     - Preprocesamiento de datos, configuración de entrenamiento y evaluación utilizando métricas de precisión y F1.

### 2. Preguntas y Respuestas (Question Answering)
   - **Descripción**: Implementa un sistema de preguntas y respuestas (QA) que responde preguntas en español, utilizando dos enfoques: QA extractivo y QA generativo.
   - **Técnicas Utilizadas**:
     - **QA Extractivo**: Emplea un modelo BERT preentrenado (`bert-base-multilingual-xquad`) para extraer respuestas de un contexto dado.
     - **QA Generativo**: Utiliza el modelo `Qwen 0.5B-Instruct` para generar respuestas en formato de texto.
     - **Few-shot prompting**: Mejora la precisión del modelo generativo proporcionando ejemplos previos en el prompt.

### 3. Técnicas de Instrucciones y Prompting
   - **Descripción**: Explora diferentes técnicas de prompting para guiar las respuestas de los modelos de lenguaje, incluyendo zero-shot, few-shot y chain of thought.
   - **Técnicas Utilizadas**:
     - **Zero-shot**: El modelo responde sin ejemplos previos.
     - **Few-shot**: Proporciona ejemplos adicionales en el prompt para mejorar el rendimiento.
     - **Chain of Thought**: Instruye al modelo a explicar su razonamiento en pasos.
     - Utilización del modelo `Qwen2.0-0.5 Instruct`, basado en la arquitectura de GPT-3.

### 4. Generación de Texto con Modelos de Lenguaje
   - **Descripción**: Explora métodos de generación de texto con el modelo `GPT-2` y diversas técnicas de sampling para controlar el estilo y la coherencia del texto.
   - **Técnicas Utilizadas**:
     - **Greedy Search** y **Beam Search**: Métodos de búsqueda para generar secuencias de texto.
     - **Sampling**: Métodos de muestreo como `Ancestral Sampling`, `Top-K Sampling` y `Nucleus Sampling` para controlar la aleatoriedad en la generación.

## Requisitos

1. **Hugging Face Transformers**
2. **Datasets** y **Evaluate** para la gestión de conjuntos de datos y evaluación.
3. **PyTorch** o **TensorFlow** como backend para los modelos de transformers.
4. (Opcional) **Google Colab** para ejecutar los notebooks con GPU.