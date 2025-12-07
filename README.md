# Análisis de Sentimiento en Reviews de Productos de Belleza

Proyecto de NLP que implementa y compara modelos de Machine Learning y Deep Learning para clasificación de sentimiento en reviews de productos de Amazon (categoría Beauty).

## Descripción

Este proyecto analiza reviews de productos de belleza utilizando el dataset Amazon Reviews 2023. Se implementan y comparan diferentes enfoques:

- **Machine Learning**: Modelos tradicionales (Regresión Logística, Random Forest, etc.)
- **Deep Learning**: Redes neuronales (LSTM, GRU)
- **Transfer Learning**: Modelo pre-entrenado de HuggingFace

## Estructura del Proyecto

```
├── 1-Carga y exploracion.ipynb      # Carga y análisis exploratorio del dataset
├── 2-Preprocesado.ipynb             # Limpieza y preprocesamiento de texto
├── 3a-Entrenamiento_Test_ML.ipynb   # Entrenamiento de modelos ML
├── 3b-Entrenamiento_Test_DeepL.ipynb # Entrenamiento de modelos DL
├── 4-Metricas_y_conclusiones.ipynb  # Evaluación y comparación de resultados
├── 5-Extra_modelo_HuggingFace.ipynb # Modelo pre-entrenado
├── utils.py                          # Funciones auxiliares
├── Inputs/data/                      # Dataset original
└── Outputs/                          # Modelos y datos procesados
```

## Dataset

- **Fuente**: [Amazon Reviews 2023](https://amazon-reviews-2023.github.io/#for-user-reviews)
- **Categoría**: All_Beauty
- **Tamaño**: ~700K reviews
- **Características**: rating (1-5), título, texto, metadatos

El dataset no está incluido en el repositorio. Descárgalo desde el enlace anterior y colócalo en `Inputs/data/All_Beauty.jsonl`.

## Instalación

Ver [SETUP.md](SETUP.md) para instrucciones detalladas de instalación.

**Requisitos rápidos**:
```bash
# Crear entorno con Python 3.11
conda create -n nlp-dl-stable python=3.11
conda activate nlp-dl-stable

# Instalar dependencias
pip install -r requirements.txt

# Registrar kernel en Jupyter
python -m ipykernel install --user --name=nlp-dl-stable
```

## Uso

Ejecuta los notebooks en orden:

1. **Exploración**: Carga y análisis del dataset
2. **Preprocesado**: Limpieza, tokenización, lematización
3. **Entrenamiento**: Modelos ML y DL
4. **Evaluación**: Métricas y comparación de resultados
5. **Extra**: Modelo HuggingFace (opcional)

## Técnicas Implementadas

**Preprocesamiento**:
- Limpieza de HTML y caracteres especiales
- Normalización de texto
- Eliminación de stopwords
- Lematización
- Tokenización

**Modelos**:
- Machine Learning: Vectorización TF-IDF + clasificadores tradicionales
- Deep Learning: Word2Vec embeddings + LSTM/GRU
- Transfer Learning: Modelos pre-entrenados

## Resultados

Los resultados detallados y métricas de comparación se encuentran en:
- `4-Metricas_y_conclusiones.ipynb`
- `Outputs/results_deep_learning.csv`

## Tecnologías

- Python 3.11
- TensorFlow/Keras
- Scikit-learn
- Gensim (Word2Vec)
- NLTK
- Pandas, NumPy
- Matplotlib, Seaborn