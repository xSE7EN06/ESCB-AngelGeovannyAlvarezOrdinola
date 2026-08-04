#  Práctica de Machine Learning — Random Forest Classifier
## Heart Disease Dataset · Clasificación Binaria

**Alumno:** Angel Geovanny Alvarez Ordinola  
**Algoritmo:** `RandomForestClassifier` (scikit-learn)  
**Tipo de Problema:** Clasificación Binaria  
**Dataset:** Heart Disease — UCI Machine Learning Repository  

---

##  Archivos del Proyecto

| Archivo | Descripción |
|---|---|
| `practica_random_forest.ipynb` | Notebook principal con el código completo |
| `README.md` | Este archivo: resumen técnico del proyecto |

---

##  Objetivo del Proyecto

Construir un modelo de Machine Learning capaz de predecir si un paciente **tiene o no tiene enfermedad cardíaca** a partir de 13 variables clínicas, utilizando el algoritmo **Random Forest** dentro de un **Pipeline de scikit-learn** que previene el *Data Leakage*.

---

##  Dataset

| Atributo | Detalle |
|---|---|
| **Fuente** | UCI Machine Learning Repository / Kaggle |
| **URL** | https://archive.ics.uci.edu/ml/datasets/Heart+Disease |
| **Registros** | ~1,025 pacientes |
| **Variables** | 13 predictoras + 1 variable objetivo |
| **Variable objetivo** | `target` (0 = Sin enfermedad · 1 = Con enfermedad) |
| **Balance de clases** | ~54% clase 1 · ~46% clase 0 (balanceado) |

### Variables del Dataset

| Variable | Tipo | Descripción |
|---|---|---|
| `age` | Numérica | Edad del paciente (años) |
| `sex` | Binaria | Sexo (1=Masculino, 0=Femenino) |
| `cp` | Categórica (0–3) | Tipo de dolor de pecho |
| `trestbps` | Numérica | Presión arterial en reposo (mm Hg) |
| `chol` | Numérica | Colesterol sérico (mg/dl) |
| `fbs` | Binaria | Azúcar en sangre en ayunas > 120 mg/dl |
| `restecg` | Categórica (0–2) | Resultado ECG en reposo |
| `thalach` | Numérica | Frecuencia cardíaca máxima alcanzada |
| `exang` | Binaria | Angina inducida por ejercicio |
| `oldpeak` | Numérica | Depresión del segmento ST |
| `slope` | Categórica (0–2) | Pendiente del segmento ST |
| `ca` | Numérica (0–3) | Vasos principales coloreados |
| `thal` | Categórica (1–3) | Resultado prueba de talasemia |
| **`target`** | **Binaria** | **Variable objetivo** |

---

##  Tecnologías Utilizadas

```
Python 3.10+
pandas          — Manipulación de datos
numpy           — Operaciones numéricas
matplotlib      — Visualizaciones base
seaborn         — Visualizaciones estadísticas
scikit-learn    — Pipeline, modelo, métricas
```

---

##  Estructura del Notebook

El notebook está organizado en **11 secciones** numeradas:

| # | Sección | Contenido |
|---|---|---|
| 1 | **Librerías** | Importación de todas las librerías necesarias |
| 2 | **Dataset** | Carga, shape, head(), info(), describe() |
| 3 | **Exploración (EDA)** | Distribución target, histogramas, boxplots, correlación, heatmap, nulos, duplicados, outliers |
| 4 | **Limpieza** | Verificación de datos, tipos, valores objetivo |
| 5 | **Preprocesamiento** | Separación X/y, nota sobre escalado |
| 6 | **División** | train_test_split 80/20 con stratify |
| 7 | **Pipeline** | Construcción con SimpleImputer + StandardScaler + RF |
| 8 | **Entrenamiento** | fit() con X_train, explicación de hiperparámetros |
| 9 | **Evaluación** | Accuracy, Precision, Recall, F1, Matriz de Confusión, ROC AUC |
| 10 | **Importancia de Variables** | feature_importances_ con gráfica ordenada |
| 11 | **Predicción Final** | 2 nuevos pacientes pasando por el pipeline |

---

##  Pipeline Implementado

```
Pipeline(steps=[
    ('imputer', SimpleImputer(strategy='median')),
    ('scaler',  StandardScaler()),
    ('clf',     RandomForestClassifier(...))
])
```

Sin Data Leakage: el fit() del preprocesamiento se realiza exclusivamente sobre X_train.

---

##  Hiperparámetros de Random Forest

| Hiperparámetro | Valor | Justificación |
|---|---|---|
| `n_estimators` | 200 | Suficientes árboles para estabilidad sin costo computacional excesivo |
| `max_depth` | 8 | Limita la profundidad para prevenir overfitting |
| `min_samples_split` | 5 | Nodos requieren al menos 5 muestras para dividirse |
| `min_samples_leaf` | 2 | Hojas con mínimo 2 muestras, suaviza el modelo |
| `max_features` | `'sqrt'` | Raíz cuadrada del total de features por árbol (criterio estándar RF) |
| `class_weight` | `'balanced'` | Ajusta pesos inversamente a la frecuencia de clase |
| `random_state` | 42 | Semilla fija para reproducibilidad total |
| `n_jobs` | -1 | Utiliza todos los núcleos CPU disponibles |

---

##  Métricas de Evaluación

El modelo fue evaluado sobre el **20% de datos de prueba** (nunca vistos durante el entrenamiento):

| Métrica | Descripción |
|---|---|
| **Accuracy** | Proporción de predicciones correctas sobre el total |
| **Precision** | De los que predijo como positivos, cuántos eran realmente positivos |
| **Recall** | De los positivos reales, cuántos fueron detectados correctamente |
| **F1 Score** | Media armónica entre Precision y Recall |
| **ROC AUC** | Capacidad discriminante del modelo (0.5=aleatorio, 1.0=perfecto) |
| **Matriz de Confusión** | Distribución de TP, TN, FP, FN |
| **Classification Report** | Métricas desglosadas por clase |
| **Curva ROC** | Trade-off TPR vs FPR con umbral óptimo (Índice de Youden) |

---

##  Predicción Final

Se simularon **2 nuevos pacientes** con perfiles clínicos distintos:

| | Paciente 1 | Paciente 2 |
|---|---|---|
| **Perfil** | Riesgo alto (hombre, 62 años, dolor asintomático) | Riesgo bajo (mujer, 45 años, sin angina) |
| **Predicción esperada** | Con Enfermedad (1) | Sin Enfermedad (0) |

Ambos pacientes pasan por el **mismo Pipeline** entrenado.

---

## ▶ Cómo Ejecutar el Notebook

### En Google Colab:
1. Ir a https://colab.research.google.com
2. Archivo → Subir notebook
3. Seleccionar `practica_random_forest.ipynb`
4. Ejecutar Runtime → Run all (Ctrl+F9)

### En Jupyter Notebook local:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
jupyter notebook practica_random_forest.ipynb
```

---

##  Buenas Prácticas Implementadas

- Código completamente comentado sección por sección
- Seguimiento de convenciones PEP8
- Nombres de variables descriptivos
- random_state=42 en todos los pasos para reproducibilidad
- stratify=y en train_test_split para mantener distribución de clases
- Pipeline que elimina Data Leakage
- Visualizaciones con etiquetas, títulos y leyendas completas
- assert para verificar invariantes del dataset
- Predicción de nuevos datos a través del pipeline completo

---

##  Requisitos

```
pandas>=1.5.0
numpy>=1.23.0
matplotlib>=3.6.0
seaborn>=0.12.0
scikit-learn>=1.2.0
```