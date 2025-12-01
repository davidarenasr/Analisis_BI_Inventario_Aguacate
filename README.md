# 🥑 Análisis de Riesgo Logístico y Optimización de Inventario (BI)

Este proyecto forma parte de la serie de **Business Intelligence (BI) y Ciencia de Alimentos** de Event Education. Demuestra cómo se aplican técnicas de Data Science para transformar datos de inventario en **decisiones de negocio** que reducen costos de almacenamiento y minimizan el riesgo de sobre-stock o agotamiento.

**Enfoque del Análisis:** Gestión del producto "Avocado Oil" (Aceite de Aguacate).

---

## 🚀 Metodología y Herramientas

### Objetivo de BI

El objetivo principal es responder a la pregunta crítica para cualquier productor o distribuidor: **¿Estamos perdiendo dinero manteniendo demasiado *stock*?**

En lugar de centrarse solo en precios históricos, este análisis se enfoca en la **eficiencia operativa** utilizando métricas clave de logística.

### Datos Utilizados

* **Fuente Principal:** `Grocery_Inventory_and_Sales_Dataset.csv` (Datos de inventario y ventas).
* **Motivación:** Se utilizó este *dataset* de 2024 para garantizar la **relevancia temporal** del análisis logístico.

### Herramientas

* **Lenguaje:** Python
* **Librerías:** `Pandas` para manipulación y cálculo de KPIs, `Plotly Express` para visualización interactiva.

---

## 📈 Indicadores Clave de Rendimiento (KPIs)

Se crearon dos KPIs fundamentales a partir de los datos brutos:

| KPI | Fórmula | Interpretación de Negocio |
| :--- | :--- | :--- |
| **Sobre-Inventario** | `Stock_Quantity` - `Reorder_Level` | **Riesgo Financiero.** Mide el capital inmovilizado. Un valor **positivo alto** indica un costo excesivo de almacenamiento. |
| **Eficiencia de Rotación** | `Sales_Volume` / `Stock_Quantity` | **Rendimiento Operativo.** Mide la rapidez con que se vende el *stock*. Un valor **bajo** (ej: $<0.5$) indica *stock* muerto o lento. |

---

## 📊 Visualización Central: Mapa de Riesgo de Inventario

El gráfico interactivo generado con Plotly es un **Diagrama de Dispersión** que clasifica cada lote o registro de inventario de "Avocado Oil" en cuadrantes de riesgo:

### Ejes

* **Eje Y (Vertical):** Sobre-Inventario (Riesgo de Costo de Almacenamiento).
* **Eje X (Horizontal):** Eficiencia de Rotación (Rendimiento del Capital).

### Zonas de Riesgo

El gráfico incluye dos líneas de referencia (umbrales de BI) que actúan como reglas de negocio:

1.  **Línea Roja (Horizontal, Y=10):** Representa el umbral donde el **Riesgo de Almacenamiento** se considera alto. Los puntos por encima de esta línea requieren acción inmediata para evitar costos excesivos.
2.  **Línea Amarilla (Vertical, X=0.5):** Representa el umbral donde la **Eficiencia de Rotación** es inaceptablemente baja. Los puntos a la izquierda indican **capital estancado**.

### Conclusión del Diagnóstico (Para el Video)

La analítica revela que los lotes en el cuadrante **Superior Izquierdo** son la **máxima prioridad**. Estos puntos tienen **alto costo de almacenamiento** y **baja rotación de ventas** simultáneamente, indicando la necesidad urgente de **ajustar los niveles de `Reorder_Level` y liberar el capital** a través de promociones.

---

### Cómo Ver el Análisis

Este repositorio contiene el archivo `.ipynb` o el script de Python que puedes ejecutar en cualquier entorno con las librerías `pandas` y `plotly` instaladas.
