# Proyecto Panama
# <center> Detección de atípicos. 

**Diseño de experimento:**

Se tienen una tabla en csv, la cual contiene 10 variables las cuales no se conoce a que hacen referencia, las cuales se trabajaran sin hacer modificaciones, ya que se desconocen su naturaleza.

Figura 1: Matriz de correlación

![alt text](https://github.com/oecorrechag/Proyecto-Panama/blob/master/corr.png)

Se observa que las variables no tienen una gran correlación por lo que se usaran todas.

Figura 2: Diagrama de dispersión

![alt text](https://github.com/oecorrechag/Proyecto-Panama/blob/master/dispersion.png)

1. Se ajustara un modelo kmedias para identificar la cantifad de subgrupos.
2. Se ajustaran 3 modelos para identificar atipicos, se cruzaran resultados para aumentar la presicion.
  * LocalOutlierFactor
  * IsolationForest
  * DBSCAN 
  * OneClassSVM (opcional)

# Objetivo

Se desarrollo un prototipo capaz de clasificar posibles transacciones anómalas (posibles fraudes). Este análisis de una base de datos de un banco la cual contiene 1000 transacciones. Se aplicaron técnicas de clasificación no supervisada.

# Resultados y conclusiones

Para identificar el número de subgrupos se utilizó Kmedias, rotando la K desde 1 hasta 20, por método del codo se tomó k = 3, también se puede utilizar método de la silueta para identificar la K optima. También se pueden utilizar métodos jerárquicos como dendrograma.

Figura 3: Método del codo

![alt text](https://github.com/oecorrechag/Proyecto-Panama/blob/master/codo.png)

Figura 4: Subgrupos

![alt text](https://github.com/oecorrechag/Proyecto-Panama/blob/master/gruposk.png)

Figura 5: Atípicos

![alt text](https://github.com/oecorrechag/Proyecto-Panama/blob/master/cruce.png)

Se optubo 1 solo posible atipico de las 1000 observaciones, lo que corresponde al 0.001%, esto esta acorde con la documentacion consultada.

### Bibliografia

* Cournapeau, D., (2007), scikit-learn. Recuperado de: https://scikit-learn.org
