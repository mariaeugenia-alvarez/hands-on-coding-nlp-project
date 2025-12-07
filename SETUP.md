# Setup del Proyecto - NLP Deep Learning

## Requisitos
- Python 3.11 (recomendado) o Python 3.10
- Conda o virtualenv

## Instalación

### Opción 1: Usando Conda (Recomendado)

```bash
# 1. Crear entorno virtual con Python 3.11
conda create -n nlp-dl-stable python=3.11

# 2. Activar el entorno
conda activate nlp-dl-stable

# 3. Instalar dependencias
pip install -r requirements.txt

# 4. Registrar el kernel en Jupyter
python -m ipykernel install --user --name=nlp-dl-stable --display-name="NLP DL (Python 3.11)"
```

### Opción 2: Usando virtualenv

```bash
# 1. Crear entorno virtual
python3.11 -m venv venv

# 2. Activar el entorno
source venv/bin/activate  # En macOS/Linux
# o
venv\Scripts\activate  # En Windows

# 3. Instalar dependencias
pip install -r requirements.txt

# 4. Registrar el kernel en Jupyter
python -m ipykernel install --user --name=nlp-dl-stable --display-name="NLP DL (Python 3.11)"
```

## Verificación

Para verificar que todo está instalado correctamente:

```python
import tensorflow as tf
import keras
import gensim
import sklearn
print(f"TensorFlow: {tf.__version__}")
print(f"Keras: {keras.__version__}")
print("✓ Todo instalado correctamente")
```

## Uso

1. Abre Jupyter Notebook o tu IDE preferido
2. Selecciona el kernel "NLP DL (Python 3.11)"
3. Ejecuta los notebooks en orden:
   - `1-Carga y exploracion.ipynb`
   - `2-Preprocesado.ipynb`
   - `3b-Entrenamiento_Test_DeepL.ipynb`

## Notas

- **Python 3.13**: TensorFlow aún no tiene soporte oficial. Usa Python 3.11 o 3.12.
- **pyDAWG**: Este paquete tiene problemas de compilación en macOS y no es necesario para este proyecto.
- Si tienes problemas con `lxml` en Linux, ejecuta: `sudo apt-get install python3-lxml`
