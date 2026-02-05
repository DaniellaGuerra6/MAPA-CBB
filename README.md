# Mapa Interactivo de Proyectos – Departamento del Atlántico

Este proyecto desarrolla un **mapa interactivo geoespacial** que permite visualizar proyectos de infraestructura y desarrollo en el **departamento del Atlántico (Colombia)**, integrando información de vías, puntos de intervención y nuevas vías proyectadas, organizadas por **categorías temáticas**.

## Capas del mapa

### 1. Municipios (capa base)
- Límites municipales del departamento del Atlántico
- Tooltip con el nombre del municipio

### 2. Municipios por MPM (opcional)
- Coloreado según el indicador **MPM**
- Escala de color continua
- Tooltip con nombre del municipio y valor MPM

### 3. Nuevas vías departamentales
- Vías proyectadas o en fase de planeación
- Visualización destacada
- Tooltip con el nombre del proyecto
- Capa independiente en el control del mapa

### 4. Proyectos por categoría temática
Incluye **vías (LINESTRING)** y **puntos (POINT)** organizados por:

- Ambiental y gestión del territorio
- Transporte
- Social y cultural
- Urbanismo y desarrollo metropolitano

Cada categoría cuenta con:
- Color propio para las vías
- Íconos personalizados para los puntos
- Tooltip unificado con el nombre del proyecto

---
## Tecnologías utilizadas

- **Python 3**
- **GeoPandas** – manejo de datos geoespaciales
- **Folium** – visualización interactiva
- **Shapely** – transformación de geometrías
- **BeautifulSoup** – limpieza de HTML
- **Branca** – escalas de color
- **Matplotlib** – paletas de colores

----
## Cómo ejecutar el proyecto

1. Instalar dependencias

```bash
pip install geopandas folium shapely branca beautifulsoup4 matplotlib
```

2. Ejecutar el script

```bash
python script_mapa.py
```

3. Abrir el archivo generado:

```text
index.html
```

---

## Resultado

El resultado final es un **mapa HTML interactivo**, con control de capas, tooltips informativos y simbología diferenciada, listo para ser usado en:

* Análisis exploratorio territorial
* Presentaciones técnicas
* Apoyo a planeación y priorización de proyectos

---

## Autora

**Daniella Gutiérrez**
Practicante de Ciencias de Datos
Empresa **POTENCIA**

---

## Notas finales

* El proyecto es modular y escalable
* Se pueden agregar nuevas categorías o capas sin modificar la estructura base
* Compatible con cualquier navegador moderno
