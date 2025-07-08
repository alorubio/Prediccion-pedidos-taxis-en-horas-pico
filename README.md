# Predicción de pedidos de taxis durante horas pico

La compañía Sweet Lift Taxi ha recopilado datos históricos sobre pedidos de taxis en los aeropuertos. Para atraer a más conductores durante las horas pico, necesitamos predecir la cantidad de pedidos de taxis para la próxima hora. Construye un modelo para dicha predicción.

La métrica RECM en el conjunto de prueba no debe ser superior a 48.

### La estructura del proyecto se basa en los siguientes pasos:
1. Descarga de datos y remuestreo por una hora.
2. Análisis de los datos
3. Entrenamiento de diferentes modelos con diferentes hiperparámetros. La muestra de prueba deberá ser el 10% del conjunto de datos inicial.
4. Prueba de los datos usando la muestra de prueba y se proporciona conclusión.

### Análisis
Durante el análisis se pudo observar que los registros tienden a subir conforme avanza el tiempo, misma situación que se visualiza en la tendencia, que se observa que va un poco en ascenso, sin embargo en el apartado de estacionalidad no se puede definir nada en concreto ya que no se observa información de manera clara con toda la data, en los residuos se puede observar que la media permanece en 0, sin embargo tiene algunos picos en ciertos momentos, sin embargo los picos no dicen nada claro, es decir, que pueda haber sucesos que nos aclare que son por tendencia o estacionalidad, por lo que no tiene estacionaridad.

Al analizar el extracto de días, se tuvo la oportunidad de visualizar en la gráfica de estacionalidad, si comparamos los resultados desde las 6:00 a las 00:00, es bastante similar, y los residuos permanecen lineales

### Pruebas y conclusiones
Se realizaron las pruebas para cada uno de los modelos que se entrenaron y se llegó a la conclusión de que para la aplicación el modelo más adecuado sería CatBoostRegressor, a pesar de que todos los modelos salieron por debajo de la métrica propuesta en la descripción del proyecto, el modelo CatBoostRegressor es el modelo que arroja el error RECM más pequeño para el conjunto de prueba, y así mismo, también un error bajo para el conjunto de entrenamiento, lo que lo hace el más idóneo a utilizar en el presente proyecto de pedidos de taxis.

**Explora los detalles del proyecto en el [repositorio completo]().**
