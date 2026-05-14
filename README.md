# Detección de Anorexia con Machine Learning en Redes Sociales

Clasificador de tweets para la detección de trastornos de la alimentación (anorexia), desarrollado para la materia de Desarrollo de Aplicaciones Avanzadas de Ciencias Computacionales (Gpo 502).

---

## Requisitos previos

- Python 3.10 o superior
- pip

---

## Instalación de dependencias

Desde la raíz del proyecto, ejecuta:

```bash
pip install -r requirements.txt
```

Luego descarga el modelo de lenguaje en español de spaCy (requerido por el notebook):

```bash
python -m spacy download es_core_news_sm
```

---

## Archivos de datos requeridos

Solo necesitas **dos archivos** de datos. Colócalos en la **raíz del proyecto** (junto al notebook):

| Archivo | Descripción |
|---|---|
| `data_train.xlsx` | Dataset de entrenamiento (etiquetado) |
| `data_test.csv` | Dataset de prueba |

> El archivo `data_train_reparado.csv` es **generado automáticamente** por el notebook durante el preprocesamiento. No es necesario proporcionarlo.

### Rutas en el notebook

Las celdas de carga de datos usan rutas absolutas. Si clonas el repositorio en una ubicación diferente, actualiza las siguientes líneas en `Clasificador.ipynb`:

```python
# Celda de preprocesamiento
input_path  = '/Users/tu_user/Documents/Reto_App_Avanzadas/data_train.xlsx'
output_path = '/Users/tu_user/Documents/Reto_App_Avanzadas/data_train_reparado.csv'

# Celda de evaluación
df_test = pd.read_csv('/Users/tu_user/Documents/Reto_App_Avanzadas/data_test.csv', ...)
Reemplaza la ruta base con la ruta absoluta a tu copia del repositorio.

---

## Ejecución

1. Asegúrate de que los archivos de datos estén en su lugar.
2. Abre `Clasificador.ipynb` con Jupyter:

```bash
jupyter notebook Clasificador.ipynb
```

3. Ejecuta las celdas en orden secuencial (**Run All** o celda por celda).

---

## Estructura del proyecto

```
Reto_App_Avanzadas/
├── Clasificador.ipynb          # Notebook principal
├── data_train.xlsx             # ← debes proveer este archivo
├── data_test.csv               # ← debes proveer este archivo
├── data_train_reparado.csv     # generado por el notebook
├── reporte_analisis_tweets.html # generado por el notebook
├── requirements.txt
└── tests/
    └── test_preprocesamiento.ipynb
```
