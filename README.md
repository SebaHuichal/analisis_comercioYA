### Resumen del Flujo de Proyecto 4 (Lecciones 1 a 6)

🎯 **Visión General del Proyecto**
El objetivo principal de este proyecto ha sido aplicar un **Análisis Exploratorio de Datos (EDA)** completo y estructurado a un caso de negocio ficticio ("ComercioYA"). El flujo abarca desde la auditoría inicial de calidad de los datos (IDA) hasta la generación de visualizaciones avanzadas y modelos estadísticos, transformando datos brutos en *insights* estratégicos para la toma de decisiones comerciales.

🛠️ **Desglose por Lección**

**1️⃣ Lección 1: Análisis Inicial de Datos (IDA)**
* **Objetivo:** Auditar la calidad estructural del dataset antes de la exploración, garantizando que la información sea confiable, coherente y libre de errores técnicos.
* **Herramientas Clave:** Pandas, NumPy.
* **Procesos Principales:**
    * **Generación del Dataset:** Construcción de la base de trabajo simulando métricas de clientes (visitas, compras, monto total, devoluciones).
    * **Clasificación:** Identificación de variables cuantitativas y categóricas.
    * **Control de Calidad:** Detección de valores nulos (pérdida de trazabilidad), inconsistencias lógicas (ej. montos negativos de -$350.0) y *outliers* extremos (compras de hasta $18,500).
* **Salida (Output):** Diagnóstico inicial que dictamina que el dataset crudo no es apto para análisis inmediato y requiere limpieza.

**2️⃣ Lección 2: Estadística Descriptiva**
* **Objetivo:** Resumir el comportamiento típico de los clientes y evaluar cómo los valores extremos (*outliers*) distorsionan las métricas del negocio.
* **Herramientas Clave:** Pandas (Métodos estadísticos).
* **Procesos Principales:**
    * **Cálculo de Métricas:** Obtención de media, mediana, moda y medidas de dispersión para el `monto_total`.
    * **Análisis de Posición:** Determinación de cuartiles y percentiles.
    * **Evaluación de Impacto:** Demostración matemática de que compras atípicas (sobre $3,754) inflan artificialmente el promedio general.
* **Salida (Output):** Recomendación técnica para la gerencia de utilizar la **Mediana** en reportes diarios de stock en lugar de la media.

**3️⃣ Lección 3: Análisis de Correlación**
* **Objetivo:** Detectar y cuantificar relaciones estadísticas entre las variables numéricas, aplicando pensamiento crítico a los resultados.
* **Herramientas Clave:** Pandas, Seaborn (Heatmaps, Scatterplots).
* **Procesos Principales:**
    * **Matriz de Correlación:** Cálculo del coeficiente de Pearson para evaluar qué variables se mueven en conjunto.
    * **Diferenciación Causal:** Análisis crítico para desmentir relaciones falsas.
* **Salida (Output):** Conclusión clave de negocio: *Correlación no es causalidad*. El alza simultánea de temperatura y devoluciones se explica por el volumen de las "Campañas de Verano", no por el clima.

**4️⃣ Lección 4: Modelado de Regresión Lineal**
* **Objetivo:** Intentar explicar o predecir la variable de ingresos (`monto_total`) a partir de variables independientes (visitas, compras) usando estadística inferencial.
* **Herramientas Clave:** Statsmodels.
* **Procesos Principales:**
    * **Modelado OLS:** Aplicación de modelos de regresión lineal simple y múltiple.
    * **Evaluación Visual y Numérica:** Análisis de la línea de tendencia y la dispersión de los puntos (clientes que gastan mucho con pocas compras y viceversa).
* **Salida (Output):** Refutación de la hipótesis. Se concluye que el modelo lineal **no sirve** para este negocio; las ventas tienen un comportamiento no lineal que depende de factores externos (estacionalidad, descuentos).

**5️⃣ Lección 5: Análisis Visual Avanzado**
* **Objetivo:** Descubrir patrones ocultos y agrupaciones complejas que los resúmenes estadísticos tradicionales pasan por alto.
* **Herramientas Clave:** Seaborn (Pairplot, Violinplot, FacetGrid).
* **Procesos Principales:**
    * **Análisis Multidimensional:** Cruce simultáneo de todas las variables coloreadas por categoría de reseña.
    * **Análisis de Densidad:** Uso de gráficos de violín para ubicar dónde se concentra realmente la masa de clientes.
* **Salida (Output):** Hallazgos críticos: La logística inversa es un problema (al llegar a 4 devoluciones, el gasto del cliente se desploma) y los *outliers* de alto gasto son clientes reales y satisfechos, ideales para programas de fidelización.

**6️⃣ Lección 6: Visualizaciones Personalizadas y Exportables**
* **Objetivo:** Tomar el control total del lienzo para crear gráficos pulidos, limpios y listos para presentaciones directivas.
* **Herramientas Clave:** Matplotlib (`plt.subplots`, `ylim`, `annotate`).
* **Procesos Principales:**
    * **Estructuración (Subplots):** Creación de tableros comparativos paralelos optimizando el espacio.
    * **Narrativa Visual:** Ajuste de límites de los ejes (para que los *outliers* no aplanen la vista general) y adición de anotaciones de texto directo en el gráfico para explicar fenómenos.
* **Salida (Entregable Final):** Reportes visuales exportados en alta resolución (PNG, PDF, SVG) listos para integrarse en presentaciones o herramientas de diseño vectorial.

🏁 **Conclusión**
El flujo de este proyecto demuestra que el análisis de datos va más allá del código. Se ha logrado transformar un conjunto de datos auditándolo desde cero, desmintiendo promedios engañosos y correlaciones falsas. El resultado final descarta predicciones simplistas (modelos lineales) a favor de *insights* visuales profundos, entregando a la empresa información clara y exportable para optimizar su logística, inventario y fidelización de clientes.
