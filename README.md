# tarea_ado
# Análisis de Variantes Somáticas en la Progresión a Carcinoma Hepatocelular (CHC)

**Autores:** José Francisco Costa Rubio, Daniel González Palazón

## Descripción del Proyecto

Este repositorio contiene los flujos de trabajo, scripts y resultados del análisis de variantes genéticas en muestras de pacientes con HCC asociado a VHC. El objetivo fue identificar las alteraciones somáticas en los estadios de cirrosis y tumor para entender mejor las bases moleculares de la enfermedad, replicando y expandiendo los hallazgos de Ikeda et al. (2014).

## Estructura del Repositorio

- **/workflow_galaxy**: Contiene el workflow de Galaxy (`.ga`) utilizado para el procesado de datos desde FASTQ hasta VCF.
- **/scripts**: Contiene el Jupyter Notebook (`.ipynb`) con todo el análisis en Python (identificación de variantes somáticas, filtrado, análisis de LEPR y generación de gráficos).
- **/data_outputs**: Contiene las tablas de datos finales generadas por los scripts, incluyendo las variantes diferenciales y la lista de genes de alta confianza.
- **/data_VEP**: Contiene los ficheros de Variant Calling obtenidos mediante la herramienta VEP de Ensembl.

## Pipeline Bioinformático en Galaxy

El procesado inicial de datos se realizó en Galaxy. Debido a que se procesó una muestra por historial, se generaron 9 historiales de análisis distintos. Todos ellos utilizaron el mismo workflow (`/galaxy/workflow.ga`).

A continuación se listan los enlaces públicos a cada historial:

### Paciente 1 (PAC1)
* **Historial Linfocito:** `https://usegalaxy.eu/u/danielgp/h/tarea-ado-pac1-linfocito`
* **Historial Cirrosis:** `https://usegalaxy.eu/u/josefrancisco/h/sanos-1`
* **Historial Tumor:** `https://usegalaxy.eu/u/danielgp/h/tarea-ado-pac1-cancer`

### Paciente 3 (PAC3)
* **Historial Linfocito:** `https://usegalaxy.eu/u/josefrancisco/h/linfocito-pac3`
* **Historial Cirrosis:** `https://usegalaxy.eu/u/josefrancisco/h/cirrotico-3`
* **Historial Tumor:** `https://usegalaxy.eu/u/danielgp/h/tarea-ado-pac3-cancer`

### Paciente 4 (PAC4)
* **Historial Linfocito:** `https://usegalaxy.eu/u/danielgp/h/tarea-ado-pac4-linfocito`
* **Historial Cirrosis:** `https://usegalaxy.eu/u/josefrancisco/h/cirrotico-4`
* **Historial Tumor:** `https://usegalaxy.eu/u/danielgp/h/tarea-ado-pac4-cancer`

## Análisis en Python

El análisis posterior se realizó con el Jupyter Notebook que se encuentra en la carpeta `/scripts`.

### Dependencias
Para ejecutar el notebook, se necesitan las siguientes librerías de Python (v.3.9):
- pandas
- matplotlib
- seaborn

