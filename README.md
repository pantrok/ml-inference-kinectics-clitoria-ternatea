# Machine-Learning-Assisted UV-Vis Inference and Kinetic Modeling of *Clitoria ternatea*

Este repositorio contiene el marco computacional completo, los conjuntos de datos empíricos y los flujos de trabajo de aprendizaje automático (Machine Learning) desarrollados para la inferencia instantánea y el modelado cinético fenomenológico de extractos hortícolas de *Clitoria ternatea*.

## Descripción del Proyecto

La extracción de compuestos bioactivos termolábiles (antocianinas y fenoles) presenta desafíos analíticos debido a la degradación térmica simultánea y los efectos de matriz. Este proyecto propone un enfoque fundamentado en **Physics-Informed Machine Learning (PIML)** para:
1. Inferir concentraciones instantáneas mitigando el ruido espectral (superando las limitaciones de la ley de Beer-Lambert).
2. Estimar constantes cinéticas de extracción ($k_{ext}$) acoplando un modelo fenomenológico de extracción-degradación con simulaciones de Monte Carlo y regresores de *Random Forest*.

## Estructura del Repositorio

El flujo de trabajo computacional está modularizado para garantizar la reproducibilidad exacta de las figuras y tablas presentadas en el artículo científico:

- `dataset.csv`: Conjunto de datos empíricos derivado del diseño factorial de extracción.
- `script_1_eda_pairplot.py`: Análisis Exploratorio de Datos (EDA) y relaciones bivariadas.
- `script_2_instantaneous_inference.py`: Inferencia multivariable con validación *Leave-One-Batch-Out* (Generación de Tabla 1 y Figura 3).
- `script_3_feature_importance.py`: Extracción de la reducción de impureza de Gini para el espacio de características (Generación de Figura 4).
- `script_4_ablation_study_global.py`: Estudio de ablación algorítmica iterativa (Generación de Figura 5).
- `script_5_augmented_kinetic_prediction.py`: Filtrado físico, aumentación de datos mediante Monte Carlo y mapeo predictivo cinético (Generación de Tablas 2 y 3, y Figura 6).
- `main_workflow.ipynb`: Cuaderno de Jupyter maestro que orquesta la ejecución secuencial de los scripts analíticos.

## Instrucciones de Instalación y Uso

1. **Clonar el repositorio:**
   ```bash
   git clone [https://github.com/usuario/clitoria-ternatea-ml-kinetics.git](https://github.com/usuario/clitoria-ternatea-ml-kinetics.git)
   cd clitoria-ternatea-ml-kinetics