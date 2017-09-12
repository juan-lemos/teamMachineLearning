# Machine Learning Team


## Caso 1 

En este caso trataremos el problema de detectar que pacientes son suceptibles de tener ataques cardíacos. Para ello utilizaremos la herramienta RapidMiner, editor de texto y Excel, además de los data set de [UCI sobre ataques cardíacos](http://archive.ics.uci.edu/ml/datasets/heart+Disease).

### Paso 1
Descargar los dataset.

[hungarian.data](http://archive.ics.uci.edu/ml/machine-learning-databases/heart-disease/hungarian.data)

[long-beach-va.data](http://archive.ics.uci.edu/ml/machine-learning-databases/heart-disease/long-beach-va.data)

[cleveland.data](http://archive.ics.uci.edu/ml/machine-learning-databases/heart-disease/cleveland.data)

[switzerland.data](http://archive.ics.uci.edu/ml/machine-learning-databases/heart-disease/switzerland.data)

### Paso 2
Transformar los datos a csv. Para ello se realizó el siguiente programa en Java.

```java
 public static void main(String[] args) throws IOException {
        formatFile("cleveland.data.txt");
        formatFile("hungarian.data.txt");
        formatFile("long-beach-va.data.txt");
        formatFile("switzerland.data.txt");

    }

    static void formatFile(String fileName) throws FileNotFoundException, IOException {
        try (BufferedReader br = new BufferedReader(new FileReader(fileName))) {
            FileOutputStream outputStream
                    = new FileOutputStream("formated_" + fileName);
            String line = "";
            while ((line = br.readLine()) != null) {
                line = line.trim();
                line = line.replace(" ", ",");
                if (!line.isEmpty()) {
                    if (line.contains("name")) {
                        outputStream.write((line+"\n").getBytes());
                    } else {
                        outputStream.write((line+",").getBytes());
                    }
                }
                System.out.println(line);
            }
            br.close();
            outputStream.close();
        }
    }

```

### Paso 3
Limpiar filas sucias en el data set de cleveland.data.csv.

### Paso 4
Agregar nombre a columnas en los csv, de acuerdo a la información que se puede apreciar en [heart-disease.names](http://archive.ics.uci.edu/ml/machine-learning-databases/heart-disease/heart-disease.names).
Esto se realiza con Excel.

### Paso 5
Estudiar cada tipo de datos como se puede apreciar en el [documento](https://github.com/juanpale/teamMachineLearning/blob/master/Ana%CC%81lisis%20Previo%20de%20datos.pdf). 

### Paso 6
Realizar un modelo en Rapid Miner como el que se aprecia en la imagen de abajo.

[Archivo_Rapid_Miner](https://github.com/juanpale/teamMachineLearning/blob/master/portfolio1.rmp).

[Represetancion en Rapid Miner](https://github.com/juanpale/teamMachineLearning/blob/master/Portfolio1Final.zip)


![Rapid_miner_process](https://raw.githubusercontent.com/juanpale/teamMachineLearning/master/Caso1.png)
