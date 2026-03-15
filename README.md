# Reducción de Dimensionalidad en Datos Clínicos Neurológicos - DataMed Analytics

Este proyecto aplica técnicas de reducción de dimensionalidad (**PCA** y **t-SNE**) sobre datos genómicos y clínicos de gliomas (LGG y GBM). El objetivo es mitigar el sobreajuste y mejorar la interpretabilidad diagnóstica, identificando patrones complejos mediante clústeres y la retención del 90% de la varianza.

## 1. Introducción
El presente reporte aborda la problemática de la alta dimensionalidad en el análisis de estudios neurológicos, específicamente enfocado en la clasificación del **Grado de Glioma**. Los gliomas son los tumores primarios más comunes del sistema nervioso central, y para este estudio, nos centramos en diferenciar dos tipos críticos extraídos del *Glioma Grading Clinical and Mutation Features Dataset* de la UCI:

* **LGG (Lower-Grade Glioma):** Gliomas de bajo grado (II y III), que presentan un crecimiento lento pero poseen un alto potencial de evolución.
* **GBM (Glioblastoma Multiforme):** Gliomas de grado IV, caracterizados por ser altamente agresivos y con una arquitectura genética compleja.

Actualmente, el equipo enfrenta desafíos de sobreajuste y baja interpretabilidad debido a que el dataset contiene múltiples mutaciones genéticas que generan ruido. Este análisis busca simplificar estos datos sin perder información crítica, facilitando la visualización de patrones complejos.



## 2. Tecnologías Utilizadas
* **Python 3.x**
* **Pandas & NumPy:** Manipulación y limpieza de datos.
* **Scikit-Learn:** Implementación de StandardScaler, PCA y t-SNE.
* **Matplotlib & Seaborn:** Visualización avanzada de datos.

## 3. Metodología
1. **Limpieza de Datos:** Unión de datasets clínicos y mutacionales, manejo de valores nulos y codificación de variables categóricas.
2. **Estandarización:** Uso de `StandardScaler` para normalizar las escalas de las mutaciones.
3. **PCA:** Reducción lineal para retener el 90% de la varianza acumulada.
4. **t-SNE:** Visualización no lineal para la identificación de clústeres biológicos.

## 4. Comparativa Técnica

| Característica | **PCA** | **t-SNE** |
| :--- | :--- | :--- |
| **Tipo de Algoritmo** | Lineal | No Lineal |
| **Enfoque** | Varianza global | Distancias locales (clústeres) |
| **Interpretación** | Ejes explican % de información | Ejes son arbitrarios |
| **Uso Principal** | Reducción de ruido | Visualización de grupos |



## 5. Resultados
Los gráficos generados en este proyecto (disponibles en la carpeta `/graficos`) demuestran que, mientras PCA es eficiente para reducir la carga computacional, t-SNE proporciona una separación mucho más clara de los grupos celulares, permitiendo identificar la "firma genética" que distingue a un LGG de un GBM.

## 6. Instalación y Uso
1. Clonar el repositorio:
   ```bash
   git clone [https://github.com/CamilaGarrido/datamed_analytics.git](https://github.com/CamilaGarrido/datamed_analytics.git)
