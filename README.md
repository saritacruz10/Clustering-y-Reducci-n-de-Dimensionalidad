# Clustering y Reducción de Dimensionalidad

## Descripción del proyecto
Este proyecto tiene como finalidad aplicar **modelos de aprendizaje no supervisado** para analizar y segmentar clientes a partir del conjunto de datos *Mall_Customers.csv*.  
Se emplean técnicas de **clustering (K-Means y DBSCAN)** y **reducción de dimensionalidad (PCA y t-SNE)** con el fin de identificar patrones de comportamiento de consumo.

---

## Dataset
- **Nombre:** Mall_Customers.csv  
- **Número de registros:** 200 clientes  
- **Variables utilizadas:**
  - `Age` (Edad)
  - `Annual Income (k$)` (Ingreso anual)
  - `Spending Score (1-100)` (Nivel de gasto)

Las columnas `CustomerID` y `Gender` no fueron utilizadas en el modelo debido a que no aportan información numérica directa para los algoritmos de clustering aplicados.

---

## Preprocesamiento de datos
Se realizaron las siguientes actividades:
- Verificación de valores nulos y registros duplicados.
- Selección de variables numéricas relevantes.
- Eliminación de columnas no necesarias.
- Normalización de los datos mediante **StandardScaler**, con el objetivo de evitar sesgos por diferencias de escala.

---

## Análisis exploratorio
Se efectuó un análisis exploratorio inicial utilizando:
- `head()`, `info()` y `describe()`
- Visualización de relaciones entre variables mediante **pairplot**

Este análisis permitió comprender la distribución de los datos y la relación entre edad, ingreso y nivel de gasto.

---

## Clustering con K-Means
- Se aplicó el **método del codo (Elbow Method)** para determinar el número óptimo de clusters.
- El punto de inflexión se identificó en **k = 4**.
- Se entrenó el modelo K-Means con dicho valor y se asignó un cluster a cada cliente.

**Resultado:** Se obtuvieron cuatro segmentos bien definidos de clientes con comportamientos diferenciados.

---

## Clustering con DBSCAN
- Se implementó el algoritmo **DBSCAN** como método alternativo de clustering.
- Este modelo
