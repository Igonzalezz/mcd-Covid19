# Practica 2
Este repositorio es un ejemplo practico de lo que se ha estado viendo en el curso "Herramientas de Productividad" impartida por el Maesto [Julio Waissman](https://github.com/jwaissman).

### Descripcion
Este proyecto contiene un Dockerfile para poder generar un contenedor con los comandos y scripts necesarios para generar una base de datos depurada (a partir de la informacion [pública](https://www.gob.mx/salud/documentos/datos-abiertos-152127) presentada por la Secretaría de Salud).

### Enfoque
Las bases de datos depuradas estan enfocadas para el analisis de la cantidad de personas infectadas con Covid-19 dentro del Municipio de Cajeme con Hipertension (Recuperadas y Fallecidas)


### Software necesario
* [Docker](https://www.docker.com/get-started)

### Instalación
#### Metodo 1
1. En consola escribir el siguiente comando para descargar la imagen.

``
docker pull osvaldo17/mcd-actividad2
``

2. Escribir el siguiente comando para generar el contenedor.

``
docker run --rm -it osvaldo17/mcd-actividad2
``

#### Metodo 2
1. Descargar el [zip file](https://github.com/Igonzalezz/mcd-Covid19/raw/main/docker.zip) y descomprimirlo.
2. En consola posicionarse en la ruta donde se descomprimio el archivo y correr el siguiente comando para generar la imagen.

``
docker build -t DatosCovid19 .
``

3. Escribir el siguiente comando para generar el contenedor.

``
docker run --rm -it DatosCovid19
``


### Archivos Finales
El script gererara 1 carpeta llamada Data dentro de la cual encontraremos estos 2 archivos para su analisis.
* Sonora_Hipertensos_Confirmados.csv
* Sonora_Hipertensos_Confirmados_Defunciones.csv

### Nota
Para la interpretacion de la informacion es necesario el Diccionario de datos que de descarga automaticamente en la carpeta "Data"
 * Catalogos.xlsx
 * Descriptores.xlsx
