# analysis-everpeak
Movilidad urbana y economía en ciudades de Latinoamérica – Sprint 5

Este repositorio contiene el análisis del Sprint 5, cuyo objetivo es evaluar cómo la movilidad urbana se relaciona con la productividad económica en las principales ciudades latinoamericanas, para identificar en qué ciudades conviene priorizar la inversión en infraestructura de transporte.

El análisis combina dos fuentes de datos:

TomTom Traffic Index (tomtom_traffic.csv): indicadores de tráfico por ciudad (retrasos por congestión, índice de tráfico, tiempos de viaje, etc.).
OECD Cities (oecd_city_economy.csv): indicadores económicos por ciudad (PIB per cápita, desempleo, PM2.5, población).
📂 Contenido del repositorio
notebooks/ladb_mobility_economy_project.ipynb → Notebook principal con carga, limpieza, unión de datasets, visualizaciones, reflexiones y resumen ejecutivo.
data/ladb_mobility_economy_2024_clean.csv → Dataset final generado por el notebook (una fila por ciudad, año 2024).
▶ Cómo abrir el notebook en Google Colab

Haz clic en el siguiente botón:

Open In Colab

O:

Abre el archivo .ipynb en GitHub.
Si tienes la extensión Open in Colab, haz clic en ella; si no, copia la URL del archivo y ábrela con el botón de arriba.
📘 Cómo reproducir el análisis
Abre notebooks/ladb_mobility_economy_project.ipynb.
Ejecuta las celdas en orden (Kernel → Restart & Run All).

Sobre los datos de entrada: el notebook original lee los archivos desde /datasets/tomtom_traffic.csv y /datasets/oecd_city_economy.csv, rutas que existen en la plataforma del curso (JupyterHub). Los CSV de origen no se incluyen en este repositorio. Para ejecutarlo en otro entorno (por ejemplo, Colab):

Sube los dos CSV de origen al entorno.
Cambia las rutas de pd.read_csv() en el Paso 1.
🧪 Pasos del análisis
Cargar y explorar los datasets de tráfico y economía.
Limpiar y preparar: estandarizar nombres de columnas a snake_case, convertir fechas y limpiar valores numéricos.
Filtrar el año 2024 en ambos datasets.
Resumir movilidad: promedios de tráfico por ciudad, país y año.
Unir movilidad y economía con un INNER JOIN por city y year.
Visualizar: boxplot de jams_delay, histograma de city_gdp_capita y gráfico de barras comparativo.
Exportar el dataset final y documentar los resultados.
📊 Cobertura de datos
Año: 2024.
15 ciudades: Belo Horizonte, Bogotá, Brasilia, Buenos Aires, Curitiba, Fortaleza, Lima, Ciudad de México, Montevideo, Porto Alegre, Recife, Río de Janeiro, Salvador, Santiago y São Paulo.
7 países: Brasil, Colombia, Argentina, Perú, México, Uruguay y Chile.
🧠 Hallazgos principales
Las ciudades con mayor congestión son Ciudad de México, São Paulo y Bogotá.
Las ciudades con mayor PIB per cápita no presentan necesariamente más congestión: no se observa una relación clara entre ambas variables.
Montevideo es un caso atípico: tiene un PIB per cápita alto y una congestión baja.
Santiago, Salvador, Fortaleza y Recife tienen un PIB per cápita bajo. La movilidad urbana no es, por sí sola, una causa de esos resultados.

Estos hallazgos son descriptivos y se basan en un solo año (2024) y 15 ciudades, por lo que no deben interpretarse como relaciones causales.

🛠️ Herramientas

Python, pandas, NumPy, seaborn y matplotlib.

🎯 Objetivo del análisis
Identificar problemas de calidad en los datos y limpiarlos.
Combinar datos de movilidad y economía en un solo dataset.
Explorar visualmente la relación entre congestión y PIB per cápita.
Generar un resumen ejecutivo con recomendaciones.
