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

4. Costo de Envío Promedio: Analiza la eficiencia logística y costos. La Tienda 1 tiene el costo de envío más alto, mientras que la Tienda 4 es la más eficiente y económica.


  <img width="875" height="535" alt="image" src="https://github.com/user-attachments/assets/2a17a05a-4011-4049-ae05-07026d7f21ab" />


5. Productos Más/Menos Vendidos: Identifica el movimiento de inventario. El volumen de ventas de productos es similar entre todas las tiendas, lo que sugiere que el problema es de valor o ejecución de ventas, no de volumen bruto de unidades.

<h2>Análisis del Desempeño Geográfico (EXTRA)</h2>

Densidad de ventas mediante coordenadas (lat y lon).
## INTERPRETACION: Análisis del Desempeño Geográfico
Al generar un gráfico de dispersión de la latitud (`lat`) y la longitud (`lon`), se observa una **clara concentración de ventas en áreas específicas**, probablemente correspondientes a las principales ciudades.

**Insight Clave:** La mayoría de las ventas se agrupan en **2 o 3 grandes cúmulos de puntos**. Si coloreamos los puntos por la `Calificación`, se puede observar si una región concentra más puntos de baja calificación (colores más oscuros), lo que podría indicar un problema regional en lugar de un problema de tienda. Este gráfico sirve para identificar los **mercados de alta densidad** y asegurar que el nuevo emprendimiento del Sr. Juan no compita directamente con una región ya saturada.
   <img width="640" height="546" alt="image" src="https://github.com/user-attachments/assets/18560462-bcf5-46f1-95ce-4b0ad891f63a" />

**INTERPRETACION EXTRA**
Utilizando el mapa interactivo generado con la librería Folium, logramos visualizar la distribución espacial de las ventas, complementando la decisión de venta.

**Hallazgos Geográficos Clave**
Concentración de Mercado: El mapa confirma que las ventas de Alura Store están fuertemente concentradas en los principales centros urbanos de Colombia (clústeres en Bogotá, Medellín, Cali). Esto indica que el éxito de las tiendas está ligado a la densidad poblacional.

**Rendimiento de la Tienda 4:** Al analizar la distribución de la Tienda 4 (identificada en el mapa), se observa que esta unidad opera en los mismos mercados clave de alta densidad que las tiendas más rentables (tienda_1, tienda_2, tienda_3).

**Implicación para la Venta**
El análisis geográfico refuerza la decisión de vender la Tienda 4. Su bajo ingreso (Análisis 1) no se debe a su ubicación, sino a factores internos (precio, ejecución, etc.), ya que comparte los mismos mercados que las unidades más exitosas.

**Al vender la Tienda 4, el Sr. Juan no perderá acceso a ningún mercado geográfico vital que no esté ya cubierto por las otras tres tiendas.**
  <img width="886" height="694" alt="image" src="https://github.com/user-attachments/assets/20a56282-d192-4303-b88b-154cbf047fb6" />

**Análisis a Profundidad:**
Para ver el análisis detallado, la comparación de indicadores entre tiendas y la justificación de la recomendación, acceda al Notebook principal: [Descargar Notebook de Análisis](analisis_alura_store_mariana_pilco_v1.ipynb).

<h2>Conclusión y Justificación (Ver Notebook)</h2>
El análisis integral reveló que la Tienda 4 es la unidad con el menor ingreso total, convirtiéndola en la principal candidata a la venta. Aunque la Tienda 1 presenta un riesgo operativo significativo (la peor calificación de cliente y el envío más caro), la recomendación se inclina por liquidar la Tienda 4 al ser la unidad menos rentable y no poseer una ventaja geográfica única sobre las otras tres.

<h2>Notas y Solución de Problemas</h2>

•	Archivos no encontrados (FileNotFoundError): Asegúrate de que los cuatro CSV estén en el mismo directorio que el notebook o que los hayas subido correctamente a Google Colab.
•	Problemas con Folium: Si el mapa interactivo no se renderiza, verifica que folium esté instalado correctamente y que estés ejecutando en un entorno compatible.

<h2>Contribuciones y Contacto</h2>

Si deseas contribuir con mejoras al análisis o agregar nuevas visualizaciones, siéntete libre de hacer un fork del repositorio y enviar un pull request.
Autora: Mariana E .Pilco
Proyecto desarrollado para el challenge de Ciencia de Datos - Alura Latam - OracleONE G9



   
