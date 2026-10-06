# Tarea 04 - Procesamiento de Lenguaje Natural

## Generación de texto a partir de reseñas de productos en español

Este repositorio contiene el desarrollo de la Tarea 04 del curso de
Procesamiento de Lenguaje Natural.

El proyecto utiliza el dataset **Amazon Reviews Multi** en español,
manteniendo continuidad con actividades anteriores del curso.

El propósito del trabajo es analizar cómo diferentes estrategias de
decodificación afectan la generación de reseñas de productos en español.

## Pregunta de investigación

**¿Cómo afectan diferentes estrategias de decodificación a la diversidad,
repetición y coherencia de textos generados por un modelo de lenguaje?**

## Dataset

Se utiliza el dataset:

`mteb/amazon_reviews_multi`

en su configuración en español.

El dataset contiene reseñas de productos de Amazon junto con sus
respectivas calificaciones.

## Estrategias de generación

Durante el experimento se compararán:

- Greedy Decoding
- Sampling
- Temperature Sampling
- Top-k Sampling
- Top-p o Nucleus Sampling

## Evaluación

Los textos generados serán comparados mediante:

- Longitud del texto
- Diversidad léxica
- Distinct-1
- Distinct-2
- Repetición
- Coherencia semántica
- Análisis cualitativo de ejemplos

## Curso

Procesamiento de Lenguaje Natural  
Maestría en Inteligencia Artificial Aplicada
