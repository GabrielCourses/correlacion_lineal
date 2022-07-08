![](https://raw.githubusercontent.com/GabrielCourses/correlacion_lineal/main/image/corr_header.png)

# Correlación lineal con Pyhon

## Introducción

La correlación lineal es un método estadístico que permite cuantificar la relación lineal existente entre dos variables. Existen varios estadísticos, llamados coeficientes de correlación lineal, desarrollados con el objetivo de medir este tipo de asociación, algunos de los más empleados son Pearson, Spearman, Kendall.

Con frecuencia, los estudios de correlación lineal preceden a análisis más complejos, como la creación de «modelos de regresión». Primero, se analiza si las variables están correlacionadas y, en caso de estarlo, se procede a generar modelos.

Es importante destacar que, la existencia de correlación entre dos variables, no implica necesariamente causalidad. La asociación puede deberse a un tercer factor <a href = "https://en.wikipedia.org/wiki/Confounding">confounder</a>.

**Correlación lineal con Python**

Existen múltiples implementaciones que permiten calcular correlaciones lineales en Python, tres de las más utilizadas están disponibles en las librerías: **SciPy**, **Pandas**, **Pingouin**.

## Coeficientes de correlación lineal

### Covarianza

Para estudiar la relación lineal existente entre dos variables continuas es necesario disponer de parámetros que permiten cuantificar dicha relación. Uno de estos parámetros es la **covarianza**, que mide el grado de variación conjunta de dos variables aleatorias.

$$Covarianza~muestral=Cov(X,Y)=\frac{\sum_{i=1}^n(x_i - \bar{x})(y_i-\bar{y})}{N-1}$$

donde $\bar{x}$ e $\bar{y}$ son la media de cada variable, y $x_i$ e $y_i$ son el valor _i-ésimo_ de las variables.

Valores positivos indican que las dos variables cambian en la misma dirección y, valores negativos, que lo hacen en direcciones opuestas.

La principal limitación de la covarianza es que, su magnitud, depende de las escalas en que se miden las variables estudiadas. Esto implica que no puede utilizarse para comparar el grado de asociación entre pares de variables medidas en distinta escala. Una forma de evitar esta limitación y poder hacer comparaciones consiste en estandarizar la covarianza, generando lo que se conoce como coeficientes de correlación.

### Coeficiente de correlación lineal

Los coeficientes de correlación lineal son estadísticos que cuantifican la asociación lineal entre dos variables numéricas. Existen diferentes tipos, de entre los que destacan el _Pearson, Rho de Spearman_ y _Tau de Kendall._ Todos ellos comparten que:

- Su valor está comprendido en el rango \[1, -1\]. Siendo 1 una correlación positiva perfecta y -1 una correlación negativa perfecta.
- Se emplea como medida de la fuerza de asociación entre dos variables(tamaño del efecto):
	+ 0: asociación nula.
	+ 0.1: asociación pequeña.
	+ 0.3: asociación mediana.
	+ 0.5: asociación moderada.
	+ 0.7: asociación alta
	+ 0.9: asociación muy alta.
	
Desde el punto de vista práctico, las principales diferencias entre estos tres coeficientes son:

- La correlación de _Pearson_ funciona bien con variables cuantitativas que tienen una distribución normal o próxima a la normal. Es más sensible a los valores extremos que las otras dos alternativas.
- La correlación de _Spearman_ se emplea con variables cuantitativas (continuas o discretas). En lugar de utilizar directamente el valor de cada variable, los datos son ordenados y reemplazados por su respectivo orden. Es un método no paramétrico muy utilizado cuando no se satisface la condición de normalidad necesaria para aplicar la correlación de Pearson.
- La correlación de _Kendall_ es otra alternativa no paramétrica que, al igual que la correlación de Spearman, utiliza la ordenación de las observaciones. Es recomendable cuando se dispone de pocos datos y muchos de ellos ocupan la misma posición en el rango, es decir, cuando hay mucha ligaduras.



