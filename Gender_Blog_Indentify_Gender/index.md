## Solución implementada para caso de estudio "Identificación de sexo por lo que se escribe en artículos"
[Volver](../index.md)

En este se busca predecir cual es el sexo de la persona que escribió una entrada de blog. Para ello utilizaremos la herramienta RapidMiner y Excel, además del [dataset](http://www.cs.uic.edu/~liub/FBS/blog-gender-dataset.rar) sobre blogs con su sexo.

### Paso 1
Descargar el dataset

### Paso 2
Limpiar con Excel el formato que tiene cada celda, ya que RapidMiner tiene problemas con el formateo que tiene las celdas del dataset original.
Además se llevaron todas las letras que identifican el género de la persona a mayúsculas y se le sacaron espacios incesarios.

### Paso 3
Leer el archivo de excel desde un bloque apropiado en RapidMiner para ello y seguido eliminar todos los missing values correspondientes a los blogs.

# SIN HACER

### Paso 4
Agregar nombre a columnas en los csv, de acuerdo a la información que se puede apreciar en [heart-disease.names](http://archive.ics.uci.edu/ml/machine-learning-databases/heart-disease/heart-disease.names).
Esto se realiza con Excel.

### Paso 5
Estudiar cada tipo de datos como se puede apreciar en el [documento](./Data%20analysis.pdf). 

### Paso 6
Realizar un modelo en Rapid Miner como el que se aprecia en la imagen de abajo.

[Archivo_Rapid_Miner](./heart_diseases_study.rmp)

[Represetanción en Rapid Miner](./Portfolio1Final.zip)

![Rapid_miner_process](./Rapidminer process screenshot.png)

[Volver](../index.md)