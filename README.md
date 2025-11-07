<h1>Análisis de Rendimiento de Tiendas para Decisión de Venta</h1>
Este proyecto realiza un análisis integral de los datos de ventas de cuatro tiendas de Alura Store para determinar cuál de ellas presenta el menor rendimiento general y, por lo tanto, debería ser considerada para su venta.
<h2>Descripción y Objetivo del Proyecto</h2>
El objetivo principal es fundamentar una decisión de negocio (venta de una unidad) mediante un riguroso Análisis Exploratorio de Datos (EDA). La recomendación final se basa en la evaluación de métricas financieras, de satisfacción del cliente, logísticas y geoespaciales.
<h2>Estructura del Repositorio y Archivos Clave</h2>

**1. analisis_alura_store_mariana_pilco_v1.ipynb**  
Notebook principal que contiene todo el proceso de **ETL (Extracción, Transformación y Carga)**, el cálculo de los **5 KPIs**, las **visualizaciones** y la **conclusión final**.

**2. base-de-datos-challenge1-latam/**  
Directorio de datos con los **cuatro archivos CSV** (`tienda_1.csv` a `tienda_4.csv`) combinados para el análisis.

**3. README.md**  
Archivo actual con los **detalles del proyecto**, las **tecnologías utilizadas** y la **guía de ejecución**.
<h2>Tecnologías y Librerías Utilizadas</h2>
El proyecto fue desarrollado en Google Colab (Python 3.10+).

**• Pandas:**  
Utilizado para la **extracción y combinación de datos** (concatenación de los cuatro archivos CSV), **limpieza de información** y **cálculo de KPIs** mediante funciones como `groupby()`, `.sum()` y `.mean()`.

**• Matplotlib / Seaborn:**  
Empleados para la **visualización descriptiva de datos**, generando **gráficos de barras y promedios** que permiten analizar los ingresos y las calificaciones de cada tienda.

**• Folium:**  
Implementado para el **análisis geoespacial complementario**, mostrando un **mapa interactivo** que visualiza la **densidad de ventas por latitud y longitud**.
<h2>Instalación y Ejecución</h2>

