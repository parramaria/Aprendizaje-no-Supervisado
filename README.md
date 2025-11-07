# APRENDIZAJE NO SUPERVISADO
Trabajo N°3
## Autor: Maria paula Sánchez 

 **1. ¿Qué es el Aprendizaje No Supervisado?**

El **aprendizaje no supervisado** es una rama del *machine learning* en la cual los algoritmos analizan conjuntos de datos **sin etiquetas predefinidas**, es decir, sin una variable objetivo conocida.  
Su propósito principal es **identificar patrones, estructuras latentes o relaciones subyacentes** en los datos, permitiendo descubrir agrupaciones o tendencias que no son evidentes a simple vista.

A diferencia del aprendizaje supervisado —donde el modelo se entrena con ejemplos que incluyen las respuestas correctas—, en el aprendizaje no supervisado **el algoritmo aprende de la estructura misma de los datos**, explorando similitudes, asociaciones o representaciones más compactas de la información.

Las técnicas más representativas de este enfoque son:

- **Clustering (Agrupamiento):** Permite agrupar observaciones con características similares (por ejemplo, *K-Means* o *DBSCAN*).  
- **Reducción de Dimensionalidad:** Transforma conjuntos de datos complejos en representaciones más simples y visualizables, preservando la mayor cantidad de información posible (por ejemplo, *PCA* o *t-SNE*).  
- **Análisis de Asociaciones:** Identifica reglas o relaciones frecuentes entre variables, como en los análisis de “cestas de mercado”.

---

 **2. Descripción del Conjunto de Datos**

Se empleó el conjunto **Wholesale Customers Data**, que recopila los **gastos anuales de clientes mayoristas** en diferentes categorías de productos.  
Las variables incluidas son:

- **Frescos:** Productos perecederos.  
- **Leche:** Productos lácteos.  
- **Comestibles:** Alimentos no perecederos.  
- **Congelados:** Productos congelados.  
- **Detergentes_Papel:** Productos de limpieza y papel.  
- **Delicatessen:** Productos gourmet o de alta gama.  
- **Canal:** Tipo de canal comercial (1 = Horeca, 2 = Retail).  
- **Región:** Ubicación geográfica (1 = Lisboa, 2 = Oporto, 3 = Otra).  

El objetivo del análisis es **segmentar a los clientes** según sus patrones de consumo, identificando grupos con características homogéneas que faciliten la comprensión de su comportamiento económico.

---

 **3. Paso a Paso del Análisis**

####  a. Carga y Exploración Inicial
- Se cargó el conjunto de datos y se examinaron las estadísticas descriptivas.  
- Se detectaron **correlaciones significativas** entre algunas variables, especialmente entre *Grocery* y *Detergents_Paper*, lo que sugiere comportamiento de consumo similar.

####  b. Preprocesamiento
- Se aplicó **StandardScaler** para estandarizar las variables y evitar sesgos por diferencias de escala.  
- Se realizó una **evaluación preliminar de dispersión** para observar la distribución y varianza de las variables principales.

####  c. Reducción de Dimensionalidad con PCA
- Se implementó el **Análisis de Componentes Principales (PCA)** para condensar la información en **dos componentes principales**, capturando la mayor parte de la varianza.  
- Esta reducción permitió **visualizar la estructura interna de los datos** y facilitar la identificación de posibles agrupamientos.

####  d. Agrupamiento con K-Means
- Se aplicó el algoritmo **K-Means** variando el número de *clusters* (k).  
- Se utilizaron el **método del codo** y el **coeficiente de silueta** para determinar el número óptimo de grupos.  
- El análisis se realizó bajo tres configuraciones:
  1. Conjunto completo de variables.  
  2. Conjunto reducido mediante PCA.  
  3. Conjunto ajustado tras eliminar variables redundantes.  

####  e. Interpretación de Resultados
- Se analizaron los **valores medios y dispersión de cada cluster**, comparándolos con las variables originales para identificar perfiles de consumo.  
- Los grupos se caracterizaron según **tipo de cliente, volumen de compra y preferencias de producto**, evidenciando comportamientos diferenciados.

---

 **4. Conclusiones**

- El aprendizaje no supervisado permitió **identificar grupos de clientes con patrones de consumo claramente diferenciados**, revelando estructuras económicas implícitas en los datos.  
- La aplicación de **PCA** demostró ser útil para **simplificar la complejidad del conjunto** sin pérdida significativa de información relevante.  
- La **reducción de variables redundantes** optimizó la eficiencia del modelo y mejoró la interpretabilidad de los resultados.  
- Se observó que algunas variables, como *Grocery* y *Detergents_Paper*, aportan información casi equivalente, lo cual sugiere su posible consolidación en análisis futuros.  
- Este enfoque constituye una **base sólida para estrategias de segmentación y marketing**, asignación eficiente de recursos y diseño de promociones dirigidas a cada perfil de cliente.



