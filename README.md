# Proyecto-DataProject-Machine-Learning.-Construccion-de-un-modelo-de-regresion-y-clasificacion

# Proyecto de Machine Learning: Modelos de Regresión y Clasificación

## Índice

1. [Introducción](#introducción)
2. [Informe Ejecutivo](#informe-ejecutivo)
3. [Estructura del Proyecto](#estructura-del-proyecto)
4. [Descripción de los Datos](#descripción-de-los-datos)
5. [Metodología](#metodología)

   1. [Preprocesado y Limpieza](#preprocesado-y-limpieza)
   2. [Ingeniería de Características](#ingeniería-de-características)
   3. [Modelado](#modelado)
6. [Resultados y Evaluación](#resultados-y-evaluación)

---

## Introducción

Este proyecto, desarrollado como parte del proyecto Machine Learning: Construcción de un modelo de regresión y clasificación, tiene como objetivo construir y comparar dos modelos de aprendizaje automático:

* **Modelo de Regresión** para predecir una variable continua relacionada con el rendimiento de un sistema mecánico.
* **Modelo de Clasificación** para identificar categorías de estado (p.ej., *funcionamiento óptimo* vs *no óptimo*).

El código se ha implementado en Python (versión ≥ 3.9) con bibliotecas de ciencia de datos estándar (pandas, scikit‑learn, NumPy, etc.). El flujo de trabajo está documentado en cuadernos Jupyter y organizado en carpetas modulares para facilitar la reproducibilidad.

---

## Informe Ejecutivo

A continuación se presenta un resumen de los principales hallazgos y métricas conseguidas. 

| Métrica                   | Regresión(train/test) | Clasificación(train/test) |
| ------------------------- | --------- | ------------- |
| **RMSE**                  | **6.59/6.47**   | –             |
| **MAE**                   | **5.28/5.27**   | –             |
| **R²**                    | **0.54/0.49**   | –             |
| **Exactitud (Accuracy)**  | –         | **0.92/0.96**     |
| **Precisión (Precision)** | –         | **0.93/0.97**     |
| **Recall**                | –         | **0.92/0.96**     |
| **F1‑Score**              | –         | **0.90/0.96**     |

---

## Estructura del Proyecto

```text
├── data/
│   ├── dataset_estudiantes.csv/               # Datos originales (.csv)
│   ├── df_clasificacion_dataproject.csv/
    └── df_regresion_dataproject.csv/         # Datos limpios/transformados
├── modelos/               # Modelos entrenados (.pkl)
│   ├── modelo_clasificacion.pkl
│   └── modelo_regresion.pkl
└── proceso/               # Cuadernos Jupyter
    ├── 01_exploracion_datos.ipynb
    └── 02_dataproject_preproceso.ipynb
    └── 03_dataproject_regresion.ipynb
    └── 04_dataproject_clasificacion.ipynb
```

---

## Descripción de los Datos

* **Variable objetivo (Regresión):** `nota_final` – variable continua entre 0 y 100.
* **Variable objetivo (Clasificación):** `aprobado` (0 = No aprobado, 1 = Aprobado).

Se incluye un análisis exploratorio inicial en `01_exploracion_datos.ipynb` que resume estadísticas descriptivas y distribuciones.

---

## Metodología

### Preprocesado y Limpieza

1. Imputación de valores faltantes (media/mediana para numéricas, moda para categóricas).
2. Detección y manejo de outliers mediante IQR y winsorización.
3. Estandarización (z‑score) y/o normalización (Min‑Max) donde procede.
4. Codificación Target para variables categóricas.

### Modelado

#### Modelo de Regresión

* **Algoritmos:** Linear Regression, Ridge, Lasso y ElasticNet.

#### Modelo de Clasificación

* **Algoritmo:** Logistic Regression.

---

## Resultados y Evaluación

### Regresión

* **Métricas(test):** RMSE = **6.47**, MAE = **5.27**, R² = **0.49**.
* **Gráficos sugeridos:** Curva de aprendizaje, Importancia de las caracteristicas.

### Clasificación

* **Métricas(test):** Accuracy = **0.96**, F1 = **0.96**, Recall = **0.96**, F1-score = **0.96**.
* **Gráficos sugeridos:** Matriz de confusión.

---


