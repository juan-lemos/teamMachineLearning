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

## [Caso de estudio - House price predicting]
En este caso buscaremos predecir el precio de una casa en base a 79 diferentes variables asociadas a la misma. Para ello utilizaremos la herramienta RapidMiner, un editor de texto y Excel, además de los data set de [House Prices: Advanced Regression Techniques](https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data).

El objetivo de este trabajo es investigar y predecir precios de inmuebles en el mercado de Ames, Iowa (USA), analizando cuáles son los factores más importantes a la hora de realizar dicha predección. La variable dependiente es justamente el precio del inmueble, en dólares  americanos. Para esto se utilizó un dataset obtenido de kaggle [House Prices: Advanced Regression Techniques](https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data). Para la preparación de los datos y construcción del modelo se utilizío la herramiento RapidMiner.

### [Habilidades demostradas]
Preparación de datos, esto implica tanto el tratamiento previo como el conocimiento del dominio del problema. 
En cuanto al tratamiento previo:
    - Detección de Outliers
    - Tratamiento de Missing Values
    - Evaluación estadísticas de los datos en el dataset

### [Atributos usados]

  
### [Solución implementada]

Para resolver el problema planteado se utilizó un modelo de regresión lineal, cuya principal característica consiste en predecir el resultado de un variable numérica. El motivo de utilizar este modelo surgue a causa de la fuerte linealidad detectada a la hora de analizar la variable dependiente del problema (precio del inmueble)

Para poder ejecutar el proceso implementado en la herramienta RapidMiner acceda al siguiente [enlace](./House prices project/index.md) y siga los pasos allí indicados.