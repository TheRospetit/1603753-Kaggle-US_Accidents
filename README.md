# 1603753-Kaggle-US_Accidents
## Universitat Autònoma de Barcelona
#### Proyecto cas Kaggle de la asignatura de Aprendizaje Computacional sobre los accidentes de tráfico en USA entre los años 2016 y 2021.  
[KAGGLE](https://www.kaggle.com/datasets/sobhanmoosavi/us-accidents?resource=download)

---

# Información del Dataset
## Descripción:
Este dataset se trata de un conjunto de datos sobre accidentes de tráfico en todo el país, que abarca 49 estados de Estados Unidos. Los datos de accidentes se recopilan desde febrero de 2016 hasta diciembre de 2021, utilizando varias API que proporcionan datos de incidentes (o eventos) de tráfico en tiempo real. Estas API difunden datos de tráfico captados por diversas entidades, como los departamentos de transporte de EE.UU. y estatales, los cuerpos de seguridad, las cámaras de tráfico y los sensores de tráfico dentro de las redes de carreteras. Actualmente, hay unos 2,8 millones de registros de accidentes en este conjunto de datos.

## Para que se puede utilizar este dataset
US-Accidents puede utilizarse para numerosas aplicaciones, como la predicción de accidentes en tiempo real, el estudio de puntos críticos de accidentes, el análisis de víctimas y la extracción de reglas de causa y efecto para predecir accidentes, o el estudio del impacto de las precipitaciones u otros estímulos ambientales en la ocurrencia de accidentes.

---

# Data cleaning
**Al analizar estos datos nos encontramos con ciertos atributos que contienen muchos Nans, dependiendo de su tamaño y el valor al que hacen referencia decidimos si eliminar el atributo directamente o rellenar los espacios con el valor de la mediana del atributo.**

**Atributo Number**

Para este atributo observamos la dispersión de sus valores mediante un boxplot
<img src="Image1/image.png" align="left" width="500" alt="Inicial Number Image"/> 
Al tener valores disparados lo que hacemos es reducir la muestra de valores eliminando aquellos en los que este atributo se dispara, seguramente debido a un error.
<img src="Image2/image.png" align="left" width="500" alt="Final Number Image"/> 

**Atributos con nans**
Mostramos los atributos con valores nan en una imágen de color
<img src="Image3/image.png" align="left" width="500" alt="Inicial Nans Image"/> 
Al ver esta distribución decido eliminar por completo la columna Number para así acabar con los problemas que puede generar.
<img src="Image4/image.png" align="left" width="500" alt="Nans without Number Image"/> 
Las columnas con nans en este nuevo caso se concentran en las columnas Wind_Chill(F) y Precipitation(in), por lo tanto en este caso lo que haremos será eliminar aquellas filas que contengan valores vacíos en una de estas dos columnas, pasando de un tamaño del dataset de **2845342** filas a **2225687** filas. Donde los datos actuales quedan de la siguiente manera:
<img src="Image5/image.png" align="left" width="500" alt="Nans without WC and PR Image"/> Como podemos ver ya no tenemos valores vacíos en nuestros datos con lo cual podemos iniciar el estudio.

# Estudios de distribuciones

