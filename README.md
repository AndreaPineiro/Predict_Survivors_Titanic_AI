# Predict_Survivors_Titanic_AI
El hundimiento del Titanic es uno de los naufragios más infames de la historia.
El 15 de abril de 1912, durante su viaje inaugural, el RMS Titanic, ampliamente considerado como "insumergible", se hundió después de chocar con un iceberg. Desafortunadamente, no había suficientes botes salvavidas para todos a bordo, lo que resultó en la muerte de 1502 de los 2224 pasajeros y tripulantes.
Si bien hubo algún elemento de suerte involucrado en la supervivencia, parece que algunos grupos de personas tenían más probabilidades de sobrevivir que otros. Con este proyecto, buscamos construir un modelo predictivo que responda a la pregunta: "¿Qué tipo de personas tenían más probabilidades de sobrevivir?" utilizando algunos datos de los pasajeros (por ejemplo: nombre, edad, sexo, clase socioeconómica, etc.). Todo el problema y los datos vienen de una competición en Kaggle, por lo que al final estaremos evaluando nuestros resultados en esa plataforma.

Realizamos una implementación en un JupyterNotebook, con el objetivo primero explorar la información que se nos daba y luego construir un modelo de aprendizaje que fuera capaz de predecir con la mayor exactitud posible el resultado de supervivencia de una persona. Nuestro script utiliza los datos de entrada ya separados en grupos de entrenamiento y prueba, especificamente utilizamos un "train.csv" y un "test.csv" para, luego de una limpieza y de llenado de datos faltantes, proceder al entrenamiento de diversos modelos de aprendizaje; arboles de decisión, bosques aleatorios, SMV, regresión logistica y al final una red neuronal. Con nuestros parametros, pudimos obtener exactitud en el 79.65% de los casos, reportado en Kaggle.

Al estar trabajando nuestra implementación del modelo predictorio, recibimos retroalimentación que nos ayudó a mejorar el modelo. Algunos de los puntos importantes se presentan a continuación:
- Buscamos generar variables que fueran más útiles a partir de lo que teníamos. Con este objetivo, generamos variables que decían si las personas iban, o no, solas con base en las variables que venian originalmente, asi como una variable categórica que buscaba dentro del nombre registrado un título como Mr, Mrs, Miss o Master. Se nos explicó cómo podemos evaluar con matrices de correlación si estas variables representaban una mejoría al modelo o no.
- Al preprocesar los datos que teníamos y ver las variables categóricas que se nos presentaban, se nos explicó la utilidad de realizar variables dummys que funcionan mejor al trabajar con modelos matemáticos. Por esa razón realizamos varios ajustes a las variables de sexo, puerta de embarque, si venían en grupo o los títulos que obtuvimos a partir de los nombres.
- Otro aspecto que se nos mencionó fue la importancia de escalar las variables para que las magnitudes fueran congruentes a lo que explicábamos y para que los modelos pudieran trabajar de mejor manera. También se nos explico que era importante realizar este escalamiento con base en el set de entrenamiento y no de prueba, para asi tener un modelo más estable y congruente.
- Por último, algo que nos fue de mucha ayuda para mejorar nuestras predicciones, fue la herramienta de redes neuronales vistas en clase. Fue muy valioso el poder trabajar y configurar la arquitectura e híperparametros que tendrían las redes, puesto que así pudimos ir obteniendo heurísticamente la configuración que nos daba mejor exactitud.
