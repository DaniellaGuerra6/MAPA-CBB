# Documentación del Proyecto

## Visualización Geoespacial de Proyectos y Vías – Departamento del Atlántico

Autor:

    Daniella Guerra - Practicante de Ciencias de Datos – POTENCIA

---

## 1. Descripción general

Este proyecto tiene como objetivo la **visualización interactiva de proyectos, vías y puntos de interés** en el departamento del Atlántico, integrando múltiples fuentes geoespaciales en un **mapa dinámico desarrollado con Python y Folium**.

El mapa permite:

* Explorar proyectos por **categoría temática**
* Visualizar **nuevas vías departamentales**
* Consultar información de proyectos directamente desde el mapa
* Activar o desactivar capas según el interés del usuario

Este desarrollo hace parte de las actividades realizadas durante la **práctica profesional en Ciencias de Datos para la empresa POTENCIA**, como apoyo al análisis territorial y a la toma de decisiones basada en datos espaciales.

---

## 2. Fuentes de datos

El proyecto integra los siguientes insumos geográficos:

* **Municipios del departamento del Atlántico**

  * Límites administrativos
  * Código y nombre del municipio
  * Indicador MPM

* **Vías**

  * Geometrías tipo `LINESTRING / LINESTRING Z`
  * Información descriptiva en formato HTML
  * Clasificación por categoría

* **Puntos**

  * Geometrías tipo `POINT`
  * Información de proyectos asociados
  * Clasificación por categoría

* **Nuevas vías**

  * Geometrías tipo `LINESTRING`
  * Nombre del proyecto asociado

---

## 3. Procesamiento de datos

Antes de la visualización, se realizan los siguientes procesos:

* Limpieza de texto HTML para extraer únicamente información relevante
* Normalización de nombres de proyectos
* Extracción del nombre del proyecto desde descripciones extensas
* Eliminación de la dimensión Z en geometrías
* Reproyección de todas las capas al sistema **EPSG:4326**
* Homologación de columnas y atributos entre capas

Estos pasos garantizan la consistencia de la información y su correcta visualización en el mapa.

---

## 4. Estructura del mapa interactivo

El mapa final incluye las siguientes capas:

### Capas base

* **Municipios**
  Visualización fija de los límites municipales con información básica.

* **Municipios por MPM** *(opcional)*
  Capa temática con escala de color para representar el indicador MPM por municipio.

### Capas de proyectos

* **Nuevas rutas**
  Visualización de nuevas vías departamentales destacadas.

* **Categorías temáticas**

  * Ambiental y gestión del territorio
  * Transporte
  * Social y cultural
  * Urbanismo y desarrollo metropolitano

Cada categoría incluye:

* Vías representadas por líneas de color
* Puntos representados con **íconos personalizados**
* Tooltips con el nombre del proyecto asociado

---

## 5. Interactividad

El usuario puede:

* Activar y desactivar capas desde el panel de control
* Consultar información de proyectos pasando el cursor sobre vías o puntos
* Comparar categorías y tipos de proyectos de forma visual

El mapa se genera como un archivo HTML independiente, listo para ser compartido o publicado.

---

## 6. Tecnologías utilizadas

* **Python**
* **GeoPandas**
* **Folium**
* **Shapely**
* **BeautifulSoup**
* **Matplotlib**
* **Branca**

---

## 7. Resultados esperados

Este proyecto permite:

* Facilitar el análisis territorial de proyectos
* Apoyar procesos de planeación y seguimiento
* Mejorar la comunicación de información geoespacial a usuarios no técnicos
* Servir como base para futuros desarrollos analíticos o dashboards geográficos

---

*Texto generado con IA