## Solución implementada para caso de estudio "House price predicting"
[Volver](../index.md)

En este caso buscaremos predecir el precio de una casa en base a 79 diferentes variables asociadas a la misma. Para ello utilizaremos la herramienta RapidMiner, un editor de texto y Excel, además del data set [House Prices: Advanced Regression Techniques](https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data).

### Paso 1 - Descargas
Descargar el data set.

[House Prices: Advanced Regression Techniques, train.csv](https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data)

### Paso 2 - Análsisis de la data
Analizar datos del data set descargado. La documentación de dicho estudio se puede ver en el siguiente [documento](./Data%20analysis.pdf). 

### Paso 3 - Implementación
Implementar modelo en RapidMiner Studio como el que se aprecia en la imagen de abajo.

[Archivo_Rapid_Miner](./heart_diseases_study.rmp)

[Represetanción en RapidMiner](./Portfolio1Final.zip)

![Rapid_miner_process](./Rapidminer process screenshot.png)

### Paso 4 - Resultados obtenidos

Testeando algoritmos con todas las columnas disponibles del dataset (con su correspondiente transformación de polinomial a numérico en caso de ser necesario).

| Algoritmo  | Parámetros |  Performance (squared correlation) |
| ---------- | ------------- | ------------- |
| Gradient Boosted Trees | number of trees: 30, maximal depth: 5  | 0.880  |
| Linear regression| feature selection: M5 prime, with bias and no colinear features (tolerance 0.05)  | 0.874  |
| W-M5P | por defecto  | 0.736  |


En base a estudio realizado de las columnas y las diversas correlaciones.

Tabla de resultados con las 10 variables más correlacionados:

| Algoritmo  | Parámetros |  Performance (squared correlation) |
| ---------- | ------------- | ------------- |
| Gradient Boosted Trees | number of trees: 30, maximal depth: 5  | 0.848  |
| Linear regression| feature selection: M5 prime, with bias and no colinear features (tolerance 0.05)  | 0.827  |
| W-M5P | por defecto  | 0.827  |

Utilizando bloque VOTE de RapidMiner:

Performance (squared correlation): 0.844

Tabla de resultados con los 6 variables que se mantienen:

| Algoritmo  | Parámetros |  Performance (squared correlation) |
| ---------- | ------------- | ------------- |
| Gradient Boosted Trees | number of trees: 30, maximal depth: 5  | 0.836  |
| Linear regression| feature selection: M5 prime, with bias and no colinear features (tolerance 0.05)  | 0.821  |
| W-M5P | por defecto  | 0.823  |

Utilizando parámetro VOTE de RapidMiner:

Performance (squared correlation): 0.836

Estas pruebas fueron realizadas sin utilizar detección de outliers.

En orden de poder comprobar que se obtienen mejores resultados una vez filtrados dichos registros detectados como outliers, volvemos a ejecutar los mismos procesos y evaluar los resultados obtenidos.

Tabla de resultados con las 10 variables más correlacionados (sin outliers):

| Algoritmo  | Parámetros |  Performance (squared correlation) |
| ---------- | ------------- | ------------- |
| Gradient Boosted Trees | number of trees: 30, maximal depth: 5  | 0.846  |
| Linear regression| feature selection: M5 prime, with bias and no colinear features (tolerance 0.05)  | 0.842  |
| W-M5P | por defecto  | 0.848  |

Utilizando parámetro VOTE de RapidMiner:

 ** Performance (squared correlation): 0.855 **

Tabla de resultados con los 6 variables que se mantienen (sin outliers):

| Algoritmo  | Parámetros |  Performance (squared correlation) |
| ---------- | ------------- | ------------- |
| Gradient Boosted Trees | number of trees: 30, maximal depth: 5  | 0.836  |
| Linear regression| feature selection: M5 prime, with bias and no colinear features (tolerance 0.05)  | 0.831  |
| W-M5P | por defecto  | 0.837 |


Utilizando parámetro VOTE de RapidMiner:

Performance (squared correlation): 0.844 

Los parámetros utilizados en los diversos modelos fueron los que obtuvieron una mejor performance para el problema planteado.

Los parámetros probados en el operador Detect Outlier Distance son los siguientes:

| Número de vecinos  | Número de outliers |  Tipo de medida |  Performance VOTE (original 0.855) |
| ---------- | ------------- | ------------- |
| 5 | 5  | Distancia euclidiana  | Distancia euclidiana | 0.853 |
| 10 | 10  | Distancia euclidiana  | Distancia euclidiana | 0.855 |
| 10 | 5  | Distancia euclidiana  | Distancia euclidiana | 0.861 |
| 10 | 3  | Distancia euclidiana  | Distancia euclidiana | 0.863 |
| 10 | 1  | Distancia euclidiana  | Distancia euclidiana | 0.855 |


** Recapitulando el mejor resultado obtenido se obtuvo utilizando las 10 variables más correlacionadas y la combinación de VOTE ya mencionada con detección de outliers (10 número de vecinos, 10 número de outliers y tipo de medición distancia euclidiana). **


Es importante recalcar que utilizando baggins para los casos de linear regression y W-M5P no se obtuvieron mejores resultados.


[Volver](../index.md)