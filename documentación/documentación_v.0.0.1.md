# Documentación del Código

En el repositorio del proyecto, se ha agregado una carpeta llamada "documentación" que contiene archivos .md (Markdown) para explicar diferentes partes del código y sus funcionalidades. Esto permitirá que el cliente comprenda y siga el desarrollo del proyecto de manera más clara.

A continuación, se muestra cómo se ha aplicado esta sugerencia al código existente:

## Importar librerías

Se importan las librerías necesarias para el análisis y visualización de datos, como pandas, seaborn y matplotlib.

## Importar funciones personalizadas

Se utiliza el comando `%run` para importar un archivo llamado "funciones_personalizadas.ipynb", que contiene funciones personalizadas utilizadas en el proyecto.

## Cargar datos

Se carga el conjunto de datos desde un archivo CSV en la ruta "/Users/andressanchez/Desktop/Data Scientist/SoyHenry/Proyecto Integrador/Data/AAPL.csv". El DataFrame resultante se guarda en la variable `df`.

### Datos en bruto

Se muestra el DataFrame `df`, que contiene los datos sin procesar.

### Datos previamente procesados

Se crea una copia del DataFrame `df` llamada `preprocessed_share_df`. Esta variable se utiliza para almacenar los datos procesados en etapas posteriores.

## Recolección y validación de datos

### ¿Qué tipo de datos son las variables en el conjunto de datos?

Se muestra el tipo de datos de cada variable en `preprocessed_share_df` utilizando el atributo `dtypes`.

Se utiliza el método `describe()` para obtener estadísticas descriptivas de las variables numéricas en el DataFrame.

Se utiliza el método `info()` para obtener información sobre el DataFrame, incluyendo el tipo de datos de cada columna y el recuento de valores no nulos.

## ¿Cuántas variables de cada tipo de datos tenemos en el conjunto de datos?

Se muestra el recuento de variables por tipo de datos en `preprocessed_share_df`.

## ¿Cuántas variables y observaciones tenemos en el conjunto de datos?

Se muestra la forma del DataFrame `preprocessed_share_df`, que indica el número de filas (observaciones) y columnas (variables).

## ¿Existen valores nulos explícitos en el conjunto de datos?

Se verifica si hay valores nulos en `preprocessed_share_df` utilizando el método `isnull()`. El resultado indica si cada variable contiene al menos un valor nulo.

## Si tenemos observaciones con valores nulos, ¿cuántos tenemos para cada variable?

Se muestra la cantidad de valores nulos para cada variable en `preprocessed_share_df` utilizando el método `isna().sum().sort_values(ascending=False)`.

## ¿Cuántos valores nulos tenemos en total en el conjunto de datos?

Se muestra la suma de todos los valores nulos en `preprocessed_share_df` utilizando el método `isnull().sum().sum()`.

## ¿Cuál es la proporción de valores nulos para cada variable?

Se visualiza la proporción de valores nulos para cada variable en `preprocessed_share_df` utilizando un gráfico de barras múltiples con Seaborn.

## ¿Cómo podemos visualizar los valores nulos en todo el conjunto de datos?

Se visualizan los valores nulos en `preprocessed_share_df` utilizando un mapa de calor con Seaborn.

Se elimina cualquier fila que contenga valores nulos en `df` utilizando el método `dropna()`.

Se muestra la parte final del DataFrame `preprocessed_share_df` para verificar los cambios.

### Verificar si hay volúmenes igual a cero disponibles

Se identifican las filas en las que la columna 'Volume' es igual a cero y se guardan en `indexZeros`. Se muestra el DataFrame filtrado utilizando `df.loc[]`.

Se crea un nuevo DataFrame llamado `price` que contiene solo la columna 'Close' de `preprocessed_share_df`. Se muestra la cabeza de `price`.

### Graficar el gráfico

Se grafica la columna 'Close' de `price` utilizando Matplotlib.

## Calcular y agregar indicadores al DataFrame

Se importan las librerías necesarias para los cálculos de indicadores, como numpy y pandas_ta.

Se calculan y agregan varios indicadores al DataFrame `preprocessed_share_df`, como RSI, promedios móviles (MA) y MACD.

Se muestra la parte final del DataFrame `preprocessed_share_df` para verificar los cambios.

