# Analisis de Tolerancia a la Glucosa con Python
Este proyecto explora la tolerancia a la glucosa comparando dos grupos de personas (jóvenes y adultos) mediante un flujo completo de carga de datos, análisis exploratorio, modelado y validación estadística. El dataset incluye:

Grupo (1 = <30 años; 2 = >30 años)

Glucosa basal (mg/dL)

Glucosa a los 60 minutos (mg/dL).

🎯 Objetivos

Describir y comparar la glucosa basal entre grupos con medidas de centralidad y dispersión, evaluando la representatividad de la media.

Analizar simetría y curtosis en adultos.

Calcular cuartiles, construir box-plots y detectar valores atípicos (grupo jóvenes).

Evaluar la normalidad de la glucosa a 60’ en ambos grupos.

Estudiar la relación lineal (basal vs. 60’) en jóvenes; ajustar regresión lineal y realizar predicción específica.

Cuantificar el porcentaje no explicado por el modelo y la sensibilidad del nivel a 60’ ante un cambio en basal.

Realizar intervalos de confianza y contrastes sobre medias y proporciones (incluye opción emparejada en adultos).

🔍 Metodología

Carga y validación de datos

Tipos, ausentes, rangos plausibles (mg/dL).

EDA por grupo (basal y 60’)

Tablas de media, mediana, desviación estándar, IQR, CV; discusión sobre asimetrías y atípicos (cuándo la media deja de ser representativa).

Distribuciones

Histogramas, QQ-plots y Shapiro–Wilk para normalidad por grupo a 60’.

Relación basal–60’ (jóvenes)

Scatter + correlación, modelo lineal (60’ ~ basal), predicción para basal = 83 mg/dL, % no explicado (1−R²) y efecto de +5 mg/dL en basal sobre 60’.

Inferencia

IC 95/99% y contrastes sobre:

media de jóvenes (basal ≈ 88 mg/dL),

diferencia de medias adultos−jóvenes (basal),

proporción con basal > 95 mg/dL y contraste p = 0,15,

(Opcional) emparejado en adultos (basal vs. 60’).

📊 Resultados principales (esperados)

Tablas comparativas de descriptivos por grupo (basal y 60’).

Gráficos: histogramas/QQ-plots, box-plots (con cuartiles y outliers), scatter con recta de ajuste.

Modelo lineal: coeficientes, R², diagnóstico básico y predicción para 83 mg/dL.

IC y p-values para las hipótesis sobre medias y la proporción >95 mg/dL.

🧱 Buenas prácticas aplicadas

Reproducibilidad (semilla donde procede).

Reporte explícito de n por grupo y supuestos de cada prueba.

Interpretación en lenguaje claro junto a cada resultado.

Gráficos con etiquetas y unidades (mg/dL) y registro opcional en figures/.

🧰 Requisitos técnicos

Python 3.9+

Jupyter Notebook o Google Colab

Paquetes: pandas, numpy, scipy, matplotlib, seaborn, statsmodels (opcional)

pip install pandas numpy scipy matplotlib seaborn statsmodels

▶️ Ejecución

Coloca el CSV en ./data/ con el nombre ARCHIVODATOSEVALUACION24csv.csv.

Abre el notebook y ejecuta todas las celdas.

Revisa las tablas y figuras generadas; opcionalmente expórtalas a figures/.

📄 Referencia del enunciado

El diseño del análisis y las preguntas de investigación siguen las especificaciones del documento adjunto (glucosa basal/60’, definición de grupos, bloques analíticos y objetivos).
