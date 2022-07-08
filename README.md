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

$$Covarianza~muestral=Cov(X,Y)=\fracc{\sum^n_{i=1}(x_i - \hat{x})(y_i-\hat{y})}{N-1}$$

