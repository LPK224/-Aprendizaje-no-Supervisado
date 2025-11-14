# 📊 Análisis de Segmentación de Clientes con Técnicas No Supervisadas

## 📌 Descripción del Proyecto
Análisis completo de clustering utilizando el dataset **Mall Customer Segmentation** que contiene información demográfica y de comportamiento de compra de 200 clientes. El objetivo es identificar segmentos naturales de clientes mediante técnicas de aprendizaje no supervisado como PCA y K-means.

## 🎯 Objetivos del Análisis
- Aplicar **Análisis de Componentes Principales (PCA)** para reducción dimensional y visualización
- Implementar **algoritmo K-means** para segmentación de clientes
- Comparar diferentes enfoques de preprocesamiento de datos
- Identificar **grupos naturales** de clientes para estrategias de marketing

## 🔧 Metodología Aplicada

### 1. Preprocesamiento de Datos
- **Limpieza**: Dataset completo sin valores nulos
- **Transformación**: Codificación de variable género (Male/Female → 0/1)
- **Estandarización**: Normalización con StandardScaler para PCA

### 2. Análisis de Componentes Principales (PCA)
- **Reducción dimensional**: 4 variables → 2 componentes principales
- **Varianza explicada**: 59.92% con dos componentes
- **Visualización**: Diagrama de dispersión 2D para identificación de patrones

### 3. Selección de Variables
- **Análisis de correlación**: No se encontraron variables redundantes (>0.7)
- **Importancia con Random Forest**: 
  - Edad: 48.88%
  - Ingreso Anual: 48.05% 
  - Género: 3.07%

### 4. Clustering con K-means
- **Evaluación múltiple**: k values de 2 a 6 clusters
- **Métricas**: WCSS y Silhouette Score
- **Comparación**: Tres versiones del dataset

## 📊 Resultados Clave

### 🏆 Mejor Configuración Identificada
- **Método**: Variables seleccionadas
- **Número óptimo de clusters**: 6
- **Calidad de agrupamiento**: Silhouette Score de 0.428
- **Variables utilizadas**: Edad, Ingreso Anual y Género

### 📈 Comparación de Métodos
| Método | Mejor K | Silhouette Score | Variables |
|--------|---------|------------------|-----------|
| Original | 6 | 0.331 | 4 |
| PCA | 4 | 0.416 | 2 |
| **Seleccionado** | **6** | **0.428** | **3** |

## 💡 Interpretación Business

### 🎯 Aplicaciones Prácticas
- **Marketing personalizado**: Estrategias específicas para cada segmento
- **Optimización de recursos**: Asignación eficiente de presupuestos comerciales
- **Desarrollo de productos**: Identificación de necesidades por segmento
- **Customer Experience**: Mejora personalizada de la experiencia de compra

### 📋 Segmentos Identificados
Los 6 clusters representan grupos de clientes con:
- Patrones de gasto similares
- Características demográficas comunes
- Comportamientos de compra diferenciados
- Potencial de valoración específico

## 🛠️ Tecnologías Utilizadas
- **Python 3.x**
- **Librerías**: pandas, numpy, scikit-learn, matplotlib, seaborn
- **Algoritmos**: PCA, K-means, Random Forest
- **Métricas**: Silhouette Score, WCSS

## 📁 Estructura del Proyecto
```
proyecto-segmentacion-clientes/
│
├── data/
│   └── Mall_Customers.csv
│
├── notebooks/
│   └── analisis_clustering.ipynb
│
├── images/
│   ├── scree_plot.png
│   ├── correlation_matrix.png
│   └── clusters_comparison.png
│
├── README.md
└── requirements.txt
```
