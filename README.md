# Tarea 04 - Procesamiento de Lenguaje Natural

## Generación de texto a partir de reseñas de productos en español

Este repositorio contiene el desarrollo de la Tarea 04 del curso de
Procesamiento de Lenguaje Natural.

## Objetivo

Analizar cómo diferentes estrategias de decodificación afectan la diversidad,
repetición y coherencia de textos generados por un modelo de lenguaje.

## Dataset

Se utilizó el dataset:

`mteb/amazon_reviews_multi`

en su configuración en español.

El corpus contiene reseñas de productos de Amazon junto con sus calificaciones.

Para el experimento se utilizó una muestra balanceada de 20.000 reseñas:

- 4.000 reseñas por cada nivel de calificación.
- 18.000 ejemplos para entrenamiento.
- 2.000 ejemplos para validación.

## Modelo

Se utilizó:

`datificate/gpt2-small-spanish`

El modelo fue ajustado mediante fine-tuning sobre el corpus de reseñas.

La pérdida de validación disminuyó aproximadamente de:

- Antes del fine-tuning: 4.99
- Después del fine-tuning: 3.02

## Estrategias evaluadas

- Greedy Decoding
- Sampling
- Temperature Sampling
- Top-k Sampling
- Top-p / Nucleus Sampling
- Top-k + Top-p

## Métricas

Se utilizaron:

- Longitud
- Distinct-1
- Distinct-2
- Repetición
- Coherencia semántica

## Principales resultados

Greedy Decoding presentó la mayor repetición y la menor diversidad.

Sampling obtuvo la mayor diversidad léxica, aunque mostró menor estabilidad
semántica.

Temperature = 0.8 ofreció un buen equilibrio entre diversidad, repetición
y coherencia.

La combinación Top-k + Top-p obtuvo la mayor coherencia semántica entre las
estrategias de muestreo evaluadas.

## Estructura

```text
NLP_Tarea_04/
│
├── README.md
├── mini_proyecto_generacion_texto.ipynb
├── data/
│   └── README.md
└── results/
    ├── README.md
    └── resumen_metricas.csv
