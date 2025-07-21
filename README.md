# <p align="center"><strong>📊 Análisis de Datos del Challenge: <em>Alura Store</em> 🛒</strong><br>
<em>**El objetivo** es identificar la tienda menos eficiente y presentar una recomendación final basada en los datos.</em></p>
## 🎯 Propósito del Análisis

Este proyecto tiene como objetivo principal ayudar al Sr. Juan, propietario de la cadena Alura Store, a tomar una decisión informada sobre **cuál de sus cuatro tiendas debe considerar vender** para iniciar un nuevo emprendimiento. Para lograr esto, se ha realizado un análisis exhaustivo de los datos de ventas, rendimiento y satisfacción del cliente de cada tienda.

El análisis busca identificar la tienda **menos eficiente** basándose en métricas clave de facturación, volumen de ventas, satisfacción del cliente y costos operativos, proporcionando una recomendación final sustentada en los datos.

---

## 📂 Estructura del Proyecto y Organización de Archivos

El proyecto está organizado de la siguiente manera:

```
Alura-Store/
├── images/
│   ├── ingresos_por_tienda.png
│   ├── mapa_calor_ingresos.png
│   └── calificacion_promedio.png
├── base-de-datos-challenge1-latam/
│   ├── tienda_1 .csv
│   ├── tienda_2.csv
│   ├── tienda_3.csv
│   └── tienda_4.csv
├── AluraStoreLatam.ipynb 
└── README.md                  
```

- **`images/`**: Esta carpeta contiene las imágenes generadas a partir del análisis de datos, incluyendo gráficos, mapas y visualizaciones clave del proyecto.
  
- **`base-de-datos-challenge1-latam/`**: Esta carpeta contiene los archivos CSV originales con los datos de ventas de cada una de las cuatro tiendas de Alura Store (`tienda_1.csv` a `tienda_4.csv`). Estos datos son la fuente principal para el análisis.
    
- **`AluraStoreLatam.ipynb`**: Este es el notebook principal (archivo de Google Colab o Jupyter) donde se realiza todo el análisis de datos. Contiene el código para cargar, limpiar, procesar y visualizar los datos, así como las conclusiones y recomendaciones.
    
- **`README.md`**: Este archivo, que estás leyendo ahora mismo, proporciona una descripción general del proyecto.
    

---

## 📊 Ejemplos de Gráficos e Insights Obtenidos

El análisis del notebook genera diversas visualizaciones y métricas clave para cada tienda. A continuación, se presentan algunos ejemplos de los tipos de gráficos y los _insights_ que se pueden extraer:

### 1. Análisis de Facturación General

Se compara el **Ingreso Total** y el **Número de Transacciones** de cada tienda.

**Insight:** La **Tienda 4** es la que presenta los ingresos totales y el número de transacciones más bajos.

***Gráfico de Ingreso Total por Tienda***
![Gráfico de Ingreso Total por Tienda](images/ingreso_total_por_tienda.png)

***Gráfico de Número de Transacciones por Tienda***
![Gráfico de Número de Transacciones por Tienda](images/transacciones_por_tienda.png)


### 2. Calificación Promedio de la Tienda

Se evalúa la **satisfacción del cliente** a través de la calificación promedio recibida.

**Insight:** La **Tienda 1** registra la calificación promedio más baja, lo que sugiere posibles problemas con la calidad del producto o el servicio al cliente, a pesar de tener un alto volumen de ventas.

***Gráfico de Calificación Promedio por Tienda***
![Gráfico de Calificación Promedio por Tienda](images/calificacion_por_tienda.png)


### 3. Costo de Envío Promedio

Se analiza la eficiencia logística comparando el costo promedio de envío por tienda.

**Insight:** La **Tienda 1** tiene el costo de envío promedio más alto, lo que indica ineficiencias logísticas o un área de servicio más costosa. Sorprendentemente, la **Tienda 4**, a pesar de sus bajos ingresos, es la más eficiente en términos de costo de envío promedio.

***Gráfico de Costo de Envío Promedio por Tienda***
![Gráfico de Costo de Envío Promedio por Tienda](images/costo_envio_por_tienda.png)


### 4. Productos Más y Menos Vendidos (por Tienda)

Se identifica qué productos tienen mayor y menor demanda en cada ubicación.

**Insight:** Este análisis revela si las tiendas están optimizando su inventario y si los productos ofrecidos se alinean con la demanda local. Por ejemplo, una tienda ineficiente podría tener sus productos "estrella" con bajas ventas, o una gran cantidad de stock de productos "menos vendidos".

***Gráfico de Top 5 Productos Más Vendidos para Tienda 1***
![Gráfico de Top 5 Productos Más Vendidos para Tienda X](images/top_productos.png)

### 5. ¡Extra! Análisis del desempeño geográfico

**Carga y procesamiento de datos geográficos por tienda**  
    Cada tienda tiene su propio conjunto de datos con:
    
    - Coordenadas (`lat`, `lon`)
        
    - Ingreso total (`ingreso_total`)
        
    - Calificación de cliente (`calificacion`)
        
    - Nombre de producto (`producto`)
        
- **Visualización con mapas interactivos usando Folium**
    
    - Se genera un **mapa base centrado en Perú**.
        
    - Cada tienda tiene un **color distinto** y un **grupo de marcadores interactivos**.
        
    - Los **CircleMarkers** tienen `popup` con información relevante.
        
- **Capa de control por tienda**  
    Puedes activar o desactivar visualmente los puntos de cada tienda por separado con `LayerControl`.
    
- **Mapa de calor (HeatMap)**  
    Se crea una capa de **HeatMap** basada en los ingresos totales (`ingreso_total`) por ubicación, lo cual:
    
    - Muestra dónde se concentran más las ventas.
        
    - Identifica áreas de alto rendimiento.

***Gráfico de mapa de calor de ingresos***
![Gráfico de mapa de calor de ingresos](images/mapa_calor_ingresos.png)

***Gráfico de datos geográficos por tienda***
![Gráfico de datos geográficos por tienda](images/vista_ubicacion_tienda_detalles.png)

---

## 🚀 Instrucciones para Ejecutar el Notebook

Para ejecutar este análisis en tu entorno de Google Colab, sigue estos pasos:

1. **Abre el Notebook:** Ve a Google Colab y abre el archivo `AluraStoreLatam.ipynb` (o el nombre que le hayas dado) desde tu repositorio de GitHub. Puedes ir a `File > Open notebook > GitHub` y pegar la URL de tu repositorio.
    
2. **Verifica las Librerías:** Asegúrate de que las librerías necesarias estén instaladas. El notebook utiliza `pandas`, `numpy`, `matplotlib`, `folium` y `seaborn`. En Google Colab, estas librerías ya vienen preinstaladas en la mayoría de los casos. Si alguna no lo está, puedes instalarla con `!pip install <nombre_libreria>`.
    
3. **Ejecuta las Celdas:** Ejecuta cada celda del notebook secuencialmente.
    
    - La primera celda cargará los datos de las URLs, y realizará la limpieza y preparación de los datos para cada tienda..
        
    - Las secciones posteriores generarán los análisis y gráficos correspondientes a cada punto (Facturación, Categorías, Calificación, Productos, Envío, Extra).
        
4. **Revisa la Salida:** Observa las tablas de resultados impresas y los gráficos generados después de ejecutar cada sección. Estos te proporcionarán los _insights_ clave para el desafío.
    

---

**Conclusión Final:**

Basado en el análisis de todas las métricas clave, la **Tienda 4** se identifica como la tienda menos eficiente. Presenta el menor **Ingreso Total**, el menor **Número de Transacciones**, el **Ticket Promedio** más bajo y el **Ingreso Promedio por Día** más bajo. Aunque es eficiente en costos de envío y tiene una calificación aceptable, su bajo rendimiento en la generación de ingresos y volumen de ventas la convierte en la principal candidata para la venta.
