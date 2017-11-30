# Machine Learning Team Portfolio

## [Caso de estudio - Enfermedades cardíacas]
El objetivo de este trabajo es investigar cuáles son los factores más importantes a la hora de predecir si una persona puede llegar a tener una enfermedad cardíaca. La variable dependiente es justamente el diágnostico de que si un paciente tiene riesgo o no de sufrir una enfermedad cardíaca. Para esto se usaron los cuatro datasets de [UCI sobre ataques cardíacos](http://archive.ics.uci.edu/ml/datasets/heart+Disease). Para la preparación de los datos se utilizo Excel y para la construcción del modelo RapidMiner.

### [Habilidades demostradas]
Preparación de datos, esto implica tanto el tratamiento previo como el conocimiento del dominio del problema. 
En cuanto al tratamiento previo:
    - Detección de Outliers
    - Tratamiento de Missing Values
    - Evaluación estadísticas de los datos en los diferentes datasets

### [Atributos usados]   
  - age : age in years
  - sex : (1 = male; 0 = female) 
  - painloc : (1 = substernal; 0 = otherwise) 
  - painexer : (1 = provoked by exertion; 0 = otherwise) 
  - relrest : (1 = relieved after rest; 0 = otherwise)
  - cp : chest pain type 
          -- Value 1: typical angina 
          -- Value 2: atypical angina 
          -- Value 3: non-anginal pain 
          -- Value 4: asymptomatic 
  - trestbps : resting blood pressure (in mm Hg on admission to the hospital) 
  - fbs : (fasting blood sugar > 120 mg/dl) (1 = true; 0 = false) 
  - restecg : resting electrocardiographic results 
                 -- Value 0: normal 
                 -- Value 1: having ST-T wave abnormality (T wave inversions and/or ST elevation or depression of > 0.05 mV) 
                 -- Value 2: showing probable or definite left ventricular hypertrophy by Estes' criteria 
  - dig : (digitalis used furing exercise ECG: 1 = yes; 0 = no) 
  - prop : (Beta blocker used during exercise ECG: 1 = yes; 0 = no) 
  - nitr : (nitrates used during exercise ECG: 1 = yes; 0 = no) 
  - pro : (calcium channel blocker used during exercise ECG: 1 = yes; 0 = no)
  - diuretic : (diuretic used used during exercise ECG: 1 = yes; 0 = no) 
  - thalach : maximum heart rate achieved 
  - thalrest : resting heart rate 
  - tpeakbps : peak exercise blood pressure (first of 2 parts) 
  - tpeakbpd : peak exercise blood pressure (second of 2 parts)  
  - trestbpd : resting blood pressure 
  - exang    : exercise induced angina (1 = yes; 0 = no) 
  - oldpeak  : ST depression induced by exercise relative to rest 
  - num      : diagnosis of heart disease (angiographic disease status) 
  
### [Solución implementada]

Para resolver el problema planteado se utilizó un modelo de regresión logística, cuya principal característica consiste en predecir el resultado de un variable categórica. En este caso dicha variable estará representada con dos posibles resultados (riesgo positivo o negativo de sufrir un ataque cardíaco).

Para poder ejecutar el proceso implementado en la herramienta RapidMiner acceda al siguiente [enlace](./First case of study - Heart diseases/index.md) y siga los pasos allí indicados.







## [Caso de estudio  - House price predicting]
En este caso buscaremos predecir el precio de una casa en base a 79 diferentes variables asociadas a la misma. Para ello utilizaremos la herramienta RapidMiner, un editor de texto y Excel, además del data set [House Prices: Advanced Regression Techniques](https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data).

El objetivo de este trabajo es investigar y predecir precios de inmuebles en el mercado de Ames, Iowa (USA), analizando cuáles son los factores más importantes a la hora de realizar dicha predección. La variable dependiente es justamente el precio del inmueble, en dólares  americanos. Para esto se utilizó un dataset obtenido de kaggle [House Prices: Advanced Regression Techniques](https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data). Para la preparación de los datos y construcción del modelo se utilizío la herramiento RapidMiner.

### [Habilidades demostradas]
Preparación de datos, esto implica tanto el tratamiento previo como el conocimiento del dominio del problema. 
En cuanto al tratamiento previo:

- Comprender el problema analizando cada una de las variables, determinando su significado y su importancia dentro del problema.
- Estudiar la variable a predecir (variable dependiente).
- Estudiar relación entre las diversas variables dependientes y la variable a predecir.
- Tratamiento de la data, pasos necesarios antes de aplicar el modelo de aprendizaje automático elegido.
- Elección de un modelo que mejor aplique al problema planteado.


### [Atributos usados]
Atributos elegidos luego de realizado el analálisis de datos correspondiente:

- SalePrice: Precio de la propiedad, en dólares. Numérico. Variable a predecir.

- OverallQual: Calidad del material utilizado en general y en el acabado de la propiedad. Numérico.
- GrLivArea: Área sobre el nivel del suelo, en pies cuadrados. Numérico.
- FullBath: Cantidad de baños completos sobre el nivel de suelo. Numérico.
- 1stFlrSF:  Área del primer piso (pies cuadrados). Numérico.
- GarageCars: Tamaño del garaje en la capacidad del automóviles. Numérico.
- GarageArea: Tamaño del garaje en pies cuadrados. Numérico.
- TotRmsAbvGrd: Cantidad de habitaciones sobre el nivel del suelo. Numérico.
- TotalBsmtSF: Área (pies cuadrados) del sótano. Numérico.
- YearBuilt: Año de construcción. Numérico.
- YearRemodAdd: Año de remodelación (misma que de construcción si no ha tenido remodelaciones). Numérico.
  
### [Solución implementada]

Para resolver el problema se planteó un algoritmo de VOTE, diseñados para mejorar la performance de los modelos tradicionales al combinar varios de ellos obteniendo varios puntos de vista del mismo problema. Dentro de los modelos utilizados en el VOTE se analizaron modelos del tipo lineal, a causa de la fuerte linealidad detectada a la hora de analizar la variable dependiente del problema (precio del inmueble), y de árboles (Gradient Boosted Trees y W-M5P, ambos caracterizados por mejorar la precisión de los resultados obtenidos).

Para poder visualizar y ejecutar el proceso implementado en la herramienta RapidMiner acceda al siguiente [enlace](./House prices project/index.md) y siga los pasos allí indicados.








## [Caso de estudio - Identificación de sexo por lo que se escribe en artículos]
El objetivo de este trabajo es investigar como realizar operaciones de text mining. Particularmente nos centraremos en un ejemplo supervisado, en el que dado una entrada de blog tenemos el sexo de la persona que escribió el texto.
Para ello se utilizó el [dataset](http://www.cs.uic.edu/~liub/FBS/blog-gender-dataset.rar) provisto por la siguiente página https://www.cs.uic.edu/~liub/FBS/sentiment-analysis.html#datasets.
Para la preparación de los datos se utilizo Excel y para la construcción del modelo RapidMiner.

### [Habilidades demostradas]
Tratamiento de entradas de texto, donde lo que entra como atributo es un texto.
Se verá como:
 - separar el texto en palabras
 - sobrepasar las variaciones que posee una misma palabra dado sus conjugaciónes
 - cómo tener en cuenta el contexto de la palabra
 las cuales poseen variantes, dado sus conjugaciones y palabras antecesoras y
 - cómo aplicar técnicas conocidas de clasificación

### [Atributos usados]
Atributos elegidos luego de realizado el analálisis de datos correspondiente:

- Blog: entrada de texto en inglés.
- Sexo: másculino o femenino.

### [Solución implementada]

Para resolver el problema se utilizaron herramientas para tokeneinizar las entradas de texto, es decir separar el texto en palabras. Luego se realizó una limpieza de la aquellas palabras o caracteres que no aportaban al problema por ejemplo salto de línea, espacios, entre otros que además son propios del idioma inglés. Seguido se utilizó stem Porter, con el objetivo de poder acortar las palabras y obtener de estas su raíz, la utilidad de esto es sobre pasar las diferentes conjugaciones que una misma palabra puede tener. Por último se generaron n gramas para tener en cuenta el contexto de la palabra.

A partir de los nuevos atributos generados (palabras), se aplicó SVM, previamente estudiando la relevacia de cada palabra para el problema de clasficación.

Para poder visualizar y ejecutar el proceso implementado en la herramienta RapidMiner acceda al siguiente [enlace](./Gender_Blog_Indentify_Gender/index.md) y siga los pasos allí indicados.








## [Caso de estudio - Aprendizaje no supervisado]
El objetivo de este trabajo es mostrar la utilización de un algoritmo no supervisado particularmente k-means. En este ejemplo analizaremos el caso de pacientes con riesgo de poseer enfermedad coronaria.

Con el objetivo de hacer un llamado de atención aquellos individuos con más riesgo. 

Para ello se utilizó el [dataset](./kMeans/k-means-cardio.csv). El cúal contiene 547 pacientes.

### [Habilidades demostradas]
Se verá como:
 - Analizar posibles outliers.
 - Utilizar el operador de RapidMiner para realizar clusterización.
 - Analizar sus posibles 
 
### [Atributos usados]
Atributos elegidos luego de realizado el analálisis de datos correspondiente:

- Peso: numérico
- Colesterol: numérico
- Sexo: binomial, masculino (representado con 1) o femenino 0

### [Solución implementada]

Para resolver el problema lo primero que se realizó fue ver si cada uno de los 3 atributos contenía outliers. Por lo que se analizo como lás gráficas de cada atributo para detectar posibles outliers.
Cómo no se detectaron outliers se paso a utilizar el operador de RapidMiner K-Means.
Se comenzó a probar diferentes k para ver cómo se formaban los cluster y que tan separados estaba uno del otro. Éste análisis se hace viendo las gráficas scatter de cada atributo con respecto al cluster que se clasifica.


Para poder visualizar y ejecutar el proceso implementado en la herramienta RapidMiner acceda al siguiente [enlace](./kMeans/index.md) y siga los pasos allí indicados.
