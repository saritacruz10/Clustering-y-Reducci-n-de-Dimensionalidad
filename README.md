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

## reprocesamiento de datos
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
- Este modelo permitió:
  - Identificar grupos basados en densidad.
  - Detectar observaciones consideradas como ruido (-1).

**Comparación:**  
Mientras K-Means asigna todos los clientes a un grupo, DBSCAN identifica clientes atípicos y genera clusters más compactos.

---

## Reducción de dimensionalidad

### PCA (Principal Component Analysis)
- Se redujo el conjunto de datos a dos componentes principales.
- Los dos componentes explican aproximadamente el **77% de la varianza total**.
- PCA facilitó la visualización y validación de la separación entre clusters.

### t-SNE
- Se aplicó t-SNE para una representación no lineal en dos dimensiones.
- Permitió observar una separación visual más clara entre los grupos.
- Se utilizó como herramienta exploratoria y de apoyo interpretativo.

---

## Interpretación de resultados
Los clusters obtenidos mediante K-Means representan los siguientes perfiles:

- **Cluster 0:** Clientes de mayor edad, ingreso medio-bajo y gasto moderado.
- **Cluster 1:** Clientes con alto ingreso y alto nivel de gasto (perfil premium).
- **Cluster 2:** Clientes jóvenes con ingreso medio y gasto elevado.
- **Cluster 3:** Clientes con alto ingreso pero bajo nivel de gasto.

Estos perfiles permiten proponer estrategias diferenciadas de segmentación y fidelización de clientes.

---

## Tecnologías utilizadas
- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Scikit-learn  
- Google Colab  

---

## 📁 Estructura del proyecto


