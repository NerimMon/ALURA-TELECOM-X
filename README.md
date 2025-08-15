# ALURA-TELECOM-X
Proyecto de Análisis de Churn en Telecom X

Objetivo del Proyecto:
Identificar patrones y factores que influyen en la evasión de clientes (Churn) de Telecom X, con el fin de proponer estrategias para mejorar la retención.

**1. Extracción de datos**

* Fuente de datos: Archivo JSON público de clientes de Telecom X.
* Herramienta utilizada: pandas en Python (pd.read_json()).
* Procedimiento:
    1.1 Se cargó el archivo JSON en un DataFrame.
    1.2 Se exploraron las columnas y se identificaron variables numéricas, categóricas y binarias.
* Términos técnicos: DataFrame, carga de datos, estructuras JSON.

**2. Transformación y normalización**

**¿Qué se hizo?**

* Se utilizó pd.json_normalize() para aplanar estructuras anidadas.
* Se separaron las variables numéricas y categóricas para análisis específico.

**Objetivo:** Preparar los datos para análisis estadístico y visualización.

**Términos técnicos:** Normalización, limpieza de datos, variables categóricas vs. numéricas.

**3. Análisis descriptivo**

**Procedimiento:**

* Uso de DataFrame.describe() para obtener estadísticas de tendencia central y dispersión.
* Exploración de variables de facturación (Factura_mensual, Total) y duración del contrato (Meses_contrato).
* Análisis de variables categóricas (Genero, Contrato, Metodo_pago) con describe() y conteos de frecuencia.
**Términos técnicos:** Media, mediana, desviación estándar, conteo de frecuencia, análisis exploratorio de datos (EDA).

  **4. Visualización de datos**

* Herramientas: matplotlib y seaborn.

* Gráficos realizados:
        4.1 Distribución de Churn: gráfico de barras y gráfico circular (pie chart) para visualizar clientes que permanecen y los que renuncian.
        4.2 Boxplots: comparación de Churn contra Factura_mensual, Total y Meses_contrato.

**Objetivo:** Detectar patrones visuales en la renuncia de clientes.
**Términos técnicos:** Gráficos de barras, pie chart, boxplot, visualización de datos, paletas de colores personalizadas.

 **5. Variables categóricas y servicios**

**¿Qué se hizo?**
* Se analizaron columnas binarias que representan servicios contratados (Servicio_telefonico, TVcable, Servicio_internet, etc.).
* Se creó una variable derivada Numero_de_Servicios sumando los servicios de cada cliente.
**Objetivo:** Medir si la cantidad de servicios contratados influye en la renuncia.
**Términos técnicos:** Variables binarias, ingeniería de características, variables derivadas.

 **6. Correlación de variables**

**Procedimiento:**
* Se convirtieron variables categóricas a variables dummy (pd.get_dummies()).
* Se calculó la matriz de correlación (.corr()) para cuantificar la relación entre variables numéricas y Churn.
* Se visualizaron los resultados con heatmaps (seaborn.heatmap()).

**Resultados clave:**
* Correlación positiva débil entre Churn y Cuentas_diarias (0.26).
* Correlación negativa fuerte entre Churn y Numero_de_Servicios (-0.6).
  
**Términos técnicos:** Variables dummy, matriz de correlación, heatmap, correlación positiva/negativa.

**7. Interpretación y conclusiones**
**Hallazgos principales:**
* Clientes con menos servicios y menor facturación tienden a renunciar.
* Contratos más cortos están asociados a mayor Churn.

**Aplicaciones prácticas:**

* Segmentación de clientes en riesgo de evasión.
* Diseño de estrategias de retención como planes combinados, ofertas personalizadas y programas de fidelización.

**Términos técnicos:** Segmentación de clientes, análisis predictivo, estrategias de retención.

**Resumen del flujo técnico**

1. Extracción de datos → JSON → DataFrame.

2. Transformación y normalización → datos limpios y separados por tipo.

3. Análisis descriptivo → estadísticas y conteos.

4. Visualización → gráficos de distribución y boxplots.

5. Ingeniería de variables → creación de Numero_de_Servicios.

6. Correlación y análisis → heatmaps y cuantificación de relaciones.

7. Interpretación → conclusiones y recomendaciones estratégicas.
