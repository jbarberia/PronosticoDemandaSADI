# PronosticoDemandaSADI
Metodologías para predecir la demanda con el uso de herramientas informacionales

# Descripción del dataset
En la carpeta `\Dataset` se encuentran los siguientes `.csv`:
- `temperatura.csv` que corresponde a los datos horarios extraidos del SMN.
- `demanda.csv` que se extrajo de la pagina de CAMMESA en la sección de informes y estadisticas.
- `dataset.csv` que es pun post-procesamiento para extraer solo una fracción de los datos.

El archivo `dataset.csv` se utilizará para el pronostico, el mismo contiene los
valores de demanda total del SADI para el rango de fechas `2021-01-01` al `2024-02-01`.
Los datos de temperatura corresponden a un promedio de los datos horarios para las
estaciones meteorologícas de Capital Federal, ya que se entiende que es el centro de 
consumo y sera más sensible a la variación de la demanda frente a esta temperatura.

La tabla del dataset con los datos a predecir (demanda) y sus variables exogenas, tiene la siguiente forma:

|fecha               | demanda     | no_habil	| temp  | es_dia_calido	|es_dia_frio  |
|--------------------|-------------|------------|-------|---------------|-------------|		
|2024-01-31 20:00:00 | 23976.806   | 0	        | 31.80	| 1           	|0            |
|2024-01-31 21:00:00 | 22933.568   | 0	        | 30.85	| 1	            |0            |
|2024-01-31 22:00:00 | 23470.519   | 0          | 30.25	| 1	            |0            |


# Objeto de estudio
Se estudia la posibilidad de utilizar la entropía de permutación para poder mejorar
o determinar algún hiperparametro que pueda mejorar la precisión (MSE) del pronostico.

---
> Parte del proyecto de investigación ASTCABA0008120 "Análisis de 
> señales basado en herramientas entrópicas en los planos informacionales".