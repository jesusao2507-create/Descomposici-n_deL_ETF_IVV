# Descomposicion_delETF_IVV
Este repositorio contiene un proyecto de analítica financiera diseñado para descomponer el rendimiento y riesgo del ETF IVV)

El proyecto combina modelado estadisticio avanzado en Python con el despliegue de una herramienta interactiva en Power BI. El flujo del proyecto se divide en tres etapas criticas:
1. Extraccion y procesamiento (Python). Descarga de datos de precios ajustados diarios mediante la API de *yfinance*. TRansformación de rendimientos logaritmicos y análisis exploratorio de datos (EDA) para identificar volatilidad, correlaciones y anomalias.
2. Modelado Econométrico (Python). Para medir las sensibilidades estructurales (Betas) de cada sector frente al  índice general se implemento una Regresión Lineal Robusta (RLM) para evaluar el impacto de *outliers* y validar estabilidad de los parametros bajo condiciones extremas del mercado. Por otra parte, se implementó un diagnostico de residuos a travez de la evaluación de supuestos mediante métricas de autocorrelación *(Durbin-Whatson)*.
3. Por ultimo, Se utilizo visualizacion a travez de Power BI para comunicar de mejor manera los hallazgos.

Tecnologías Utlizadas.
- Python 3.x
    - yfinance (ingesta de datos financieros)
    - Pandas y Numpy (manipulacion de series temporales)
    - statsmodels (Regesión lineal OLS y RLM, pruebas estadisticas)
    - matplotlib y seaborn (Análisis Visual de resiudos y correlación)
- Power BI Desktop

Estructura del repositorio
1. /data: contiene los archivos .csv procesados y listos para su uso en inteligencia de negocios.
2. /notebooks: Jupyter Notebook con el script documentaod paso a paso, desde la descarga de datos hasta las pruebas estadisticas de la regresión.
3. /dashboard: Archivo .pbix de Power BI listo para visualizacion e interacción.
