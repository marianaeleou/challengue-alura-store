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

## Guía de Instalación
Para ejecutar el proyecto en tu entorno local o en Google Colab:

1. **Clonar el repositorio:**
   ```bash
   git clone https://github.com/angelesGladin/challenge-data-science.git
2. **Instalar las dependencias necesarias:**
   ```bash
   pip install pandas matplotlib seaborn folium
## Guía de Ejecución
1.	Abre el archivo AluraStoreLatam.ipynb en Google Colab o Jupyter Notebook.
2.	Asegúrate de subir los cuatro archivos CSV (contenidos en el directorio base-de-datos-challenge1-latam) a tu entorno de Colab/Jupyter para que el código de carga funcione.
3.	Ejecuta todas las celdas de forma secuencial (Run All o Shift + Enter) para replicar el análisis completo.
   
<h2>Métricas Clave Analizadas</h2>

1. Ingreso Total por Tienda: Mide la rentabilidad financiera directa. El hallazgo principal es que la Tienda 4 registra consistentemente los ingresos más bajos, lo que la convierte en la principal candidata a la venta por criterios financieros.
   
   <img width="886" height="508" alt="image" src="https://github.com/user-attachments/assets/a8dd07d0-b7d3-4ff7-892c-15dc5dbd1607" />


2. Ventas por Categoría: Revela los productos más populares. Todas las tiendas comparten las mismas tres categorías principales, indicando que la baja rentabilidad de la Tienda 4 no es un problema de surtido.

3. Valoración Media por Tienda: Evalúa la satisfacción del cliente (CSAT). La Tienda 1 tiene la peor calificación promedio, señalando problemas subyacentes de calidad o servicio a pesar de sus altos ingresos.


 <img width="886" height="526" alt="image" src="https://github.com/user-attachments/assets/9de8a822-ea67-4d3b-b770-1f3f479fbaa3" />

5. Costo de Envío Promedio: Analiza la eficiencia logística y costos. La Tienda 1 tiene el costo de envío más alto, mientras que la Tienda 4 es la más eficiente y económica.


  <img width="875" height="535" alt="image" src="https://github.com/user-attachments/assets/2a17a05a-4011-4049-ae05-07026d7f21ab" />


7. Productos Más/Menos Vendidos: Identifica el movimiento de inventario. El volumen de ventas de productos es similar entre todas las tiendas, lo que sugiere que el problema es de valor o ejecución de ventas, no de volumen bruto de unidades.
