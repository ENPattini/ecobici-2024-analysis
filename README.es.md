# Movilidad Urbana en Buenos Aires: Análisis con R y Tableau (Ecobici 2024)

Este proyecto analiza más de 3.2 millones de viajes del sistema público de bicicletas Ecobici de Buenos Aires en 2024 para descubrir patrones de uso, demanda máxima, estaciones populares y oportunidades para mejorar la movilidad urbana sostenible.


## Hallazgos Principales

- Fuerte foco en commuting: pico vespertino (16–18 hs, hasta 308k viajes/hora) y secundario matutino (7–10 AM).  
- Promedio en días hábiles ~10.724 viajes/día vs ~4.081 en fines de semana (ratio ~2.6:1).  
- Estaciones de origen top (Constitución 35k, Pacífico 34k) y heatmaps espaciales muestran demanda concentrada en áreas centrales (Microcentro, Palermo, Recoleta).  
- Orígenes matutinos se agrupan en zonas residenciales/centrales, destinos vespertinos se dispersan, confirmando commuting bidireccional.  
- Duración de viajes: mediana ~16.1 min, promedio ~21.7 min — la mayoría bajo 30 min.  
- Distribución por género: Masculino ~60.8%, Femenino ~31.6%.  
- Picos estacionales en primavera tardía/verano temprano (octubre 335k), mínimo en invierno (julio 215k).  
- Flujos netos extremos (ej. Juan Manuel De Blanes +3.056, Cerrito -2.064) destacan necesidades de rebalanceo.


## Dashboard Interactivo

Explora el dataset completo de forma interactiva en Tableau Public:  
[Ver el Dashboard Ecobici 2024](https://public.tableau.com/views/Ecobici2024-InteractiveUrbanBike-SharingInsights/Ecobici2024-UrbanBike-SharingInsights?:language=es-ES&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)


## Reporte HTML Completo

**Reporte HTML Completo** (con heatmaps interactivos):  
[Abrir el Reporte Online](https://www.emilionahuelpattini.com/es/data/data-analysis/projects/ecobici-2024/urban-mobility-analysis.html) (Versión interactiva con zoom, pan y tooltips. Sin necesidad de descarga.)  

**Alternativa (descarga offline)**: Descarga el ZIP del repositorio y abre `outputs/urban-mobility-analysis.html` (requiere la carpeta `outputs/urban-mobility-analysis_files/`).

**Reporte PDF Completo** (versión imprimible):

[Descargar Reporte PDF](https://www.emilionahuelpattini.com/es/data/data-analysis/projects/ecobici-2024/urban-mobility-analysis.pdf)  
(Reporte completo con todos los visuales e insights — versión estática, ~12 páginas)


## Habilidades Demostradas

- Limpieza y preparación de datos (R, tidyverse, lubridate)  
- Análisis Exploratorio de Datos (temporal, espacial, demográfico)  
- Visualización: ggplot2, leaflet (heatmaps interactivos), Tableau  
- Insights y recomendaciones accionables para el negocio  
- Reproducibilidad y documentación


## Fuente de Datos

Portal oficial de datos abiertos de Buenos Aires (público y gratuito):

- Datos crudos: https://data.buenosaires.gob.ar/dataset/bicicletas-publicas (descargar "ecobici_recorridos_realizados_2024.csv")  
- Datos procesados: El CSV limpio (trips_clean_2024.csv) no se incluye por límites de tamaño de GitHub (>100 MB). Puedes recrearlo ejecutando el reporte R Markdown (urban-mobility-analysis.Rmd) o pedírmelo.`


## Cómo Reproducir

1. Clonar este repositorio.
2. **Descargar los datos crudos** (no incluidos por tamaño):  
   Desde la fuente oficial: https://data.buenosaires.gob.ar/dataset/bicicletas-publicas  
   Descargar "ecobici_recorridos_realizados_2024.csv" y colocarlo en `data/raw/`.
3. Abrir `urban-mobility-analysis.Rmd` en RStudio. 
4. Instalar paquetes necesarios (una sola vez):  
   ```r
   install.packages(c("tidyverse", "lubridate", "scales", "leaflet", "leaflet.extras", "here"))
   ```
5. Knit para generar el reporte (HTML/PDF).
6. Tableau: Importar `data/processed/trips_clean_2024.csv` para recrear o explorar los visuales interactivos (heatmaps, peak hours, etc.).
