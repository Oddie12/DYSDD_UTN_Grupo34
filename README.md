# Deteccion de Fallas en Sensores IoT Industriales

Proyecto Final Integrador — Diplomado en Ciencia de Datos y Analisis Avanzado (UTN FRBA)

## Descripcion

Modelo de clasificacion que identifica estados operativos de alto riesgo de falla en maquinaria industrial, a partir de lecturas de temperatura, velocidad rotacional, torque y desgaste de herramienta. Utiliza el dataset AI4I 2020 Predictive Maintenance (UCI ML Repository).

## Resultados principales

- **Modelo elegido:** Random Forest con variables de dominio y pesos de clase
- **Recall:** 85.3% (detecta 58 de 68 fallas en prueba)
- **Precision:** 75.3% (3 de cada 4 alertas son correctas)
- **Ahorro estimado:** 74% vs mantenimiento reactivo (escenario central 10:1)

## Estructura del repositorio

```
.
├── TP_Final_Anomalias_IoT.ipynb   # Notebook principal (Colab / Jupyter)
├── ai4i2020.csv                   # Dataset (se descarga automaticamente si no existe)
├── figuras/                       # Figuras generadas por el notebook
│   ├── comparativa_modelos.png
│   ├── costo_umbral.png
│   └── matriz_confusion_test.png
├── Informe_Final_Deteccion_Fallas_IoT.pdf
├── requirements.txt
└── README.md
```

## Como ejecutar

### Opcion 1: Google Colab (recomendado)

1. Abrir `TP_Final_Anomalias_IoT.ipynb` en Google Colab.
2. Subir `ai4i2020.csv` cuando se solicite, o dejar que el notebook lo descargue desde UCI.
3. Ejecutar todas las celdas en orden (Runtime > Run all).

### Opcion 2: Ejecucion local

```bash
# Clonar el repositorio
git clone <URL_DEL_REPO>
cd <NOMBRE_DEL_REPO>

# Crear entorno virtual (opcional pero recomendado)
python -m venv venv
source venv/bin/activate  # Linux/Mac
# venv\Scripts\activate   # Windows

# Instalar dependencias
pip install -r requirements.txt

# Abrir el notebook
jupyter notebook TP_Final_Anomalias_IoT.ipynb
```

## Dependencias

- Python >= 3.9
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- xgboost
- imbalanced-learn
- ucimlrepo

## Dataset

**AI4I 2020 Predictive Maintenance Dataset**
- Fuente: [UCI Machine Learning Repository](https://doi.org/10.24432/C5HS5C)
- Autor: Matzka, S. (2020)
- Licencia: CC BY 4.0
- 10,000 registros, 14 columnas, sin valores faltantes

## Autores

- Juan Marcelo Saumell
- Axel Carcia
- Juan Ignacio Figueiras
- Luis Ignacio Alaniz Bellotti
- Santino Martins

## Licencia

Este proyecto es un trabajo academico. El dataset utilizado tiene licencia CC BY 4.0.
