# 📊 Análisis de Ventas y Predicción con Machine Learning (2024 - 2026)

Este proyecto realiza un análisis exploratorio de datos (EDA) y desarrolla modelos de Machine Learning para segmentar y predecir el comportamiento de ventas de diferentes proveedores avícolas hacia el inicio del año 2026.

## 🚀 Tecnologías Utilizadas
* **Python** (Core del proyecto)
* **Pandas & NumPy** (Manipulación y limpieza de datos)
* **Matplotlib & Seaborn** (Visualización estadística)
* **Scikit-learn** (Modelado predictivo con Regresión Lineal)

---

## 📈 Descubrimientos Clave (Insights de Negocio)

Tras analizar el histórico de los años 2024 y 2025, se obtuvieron las siguientes conclusiones estratégicas:

### 1. Comportamiento Anual 📅
* **Año con mayores ventas:** **2025** lideró el histórico con un total de **$696,204.18 MXN**, mostrando un crecimiento positivo frente a los **$681,222.41 MXN** registrados en **2024**.

### 2. Análisis por Día de la Semana 🕒
* El consumo fuerte se concentra en el cierre y arranque de semana. 
* El **Domingo** es el día con mayor volumen de venta acumulada (**$202,830.02 MXN**), seguido muy de cerca por el **Lunes** (**$202,462.53 MXN**).

---

## 🤖 Modelado y Predicciones para la Semana 1 de 2026

En lugar de utilizar un modelo global que promediara a todo el mercado a ciegas, se optó por una **segmentación individualizada** entrenando un modelo de `LinearRegression` exclusivo para cada empresa. 

Las predicciones estiman el **valor promedio por transacción individual (lote de mayoreo)** para la primera semana de 2026:

* **POLLOS ANDINOS:** `$70.95 MXN` (Mantiene el ticket promedio por venta más alto).
* **AVÍCOLA DEL NORTE:** `$67.71 MXN`
* **DISTRIBUIDORA CENTRAL:** `$66.57 MXN` (Presenta transacciones ligeramente más económicas que el promedio general).

> 💡 **Nota metodológica:** Los modelos analizan el comportamiento transaccional fila por fila. Para predecir el volumen de ingresos totales acumulados por semana, se recomienda aplicar una agregación previa con `.groupby()` sobre la variable temporal.

---

## 🛠️ Cómo Ejecutar el Proyecto
1. Asegúrate de tener instalado Jupyter Notebook o una extensión compatible en VS Code.
2. Clona el repositorio e instala las dependencias:
   ```bash
   pip install pandas numpy matplotlib scikit-learn
   ```