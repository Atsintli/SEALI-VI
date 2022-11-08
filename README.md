# SEALI-VI
Sistema de Escucha Automática para la Libre Improvisación V.1

En esta investigación he expuesto diversas metodologías que permiten explorar tecnologías como el aprendizaje y la escucha de máquina aplicadas al análisis de bases de datos de improvisaciones libres. Estos desarrollos me permitieron crear un sistema sonoro que escucha e interactúa en tiempo real consigo mismo o con otros músicos, adaptando sus respuestas al contexto sonoro de acuerdo con la base de datos de entrenamiento. La configuración del sistema contempla dos fases, la primera se concentra en el análisis espectral del sonido e incluye varios procesos algorítmicos: la captura de una fuente sonora que es transformada en audio digital, la segmentación del audio, el análisis espectral a través de la extracción de características, la clasificación sin supervisión para crear una base de datos y la creación con redes neuronales profundas de un modelo supervisado aplicado a la predicción sonora en tiempo real. La segunda se centra en el análisis estructural musical a varios niveles y contempla: el análisis de descripciones numéricas del audio en forma de series de tiempo mediante el algoritmo LSTM para aproximarse a la identificación de estructuras musicales dentro de la práctica particular de algunos improvisadores libres. A su vez, las interacciones de este sistema conjuntan tres funciones. El primero se concentra en la predicción, búsqueda y reproducción, de archivos de audio midiendo el índice de similitud comparando entre lo escuchado y la base de datos de entrenamiento. El segundo, también realiza la predicción y búsqueda de archivos similares que envía a través del protocolo OSC para ser utilizados por Supercollider y aplica distintos procesamientos a los audios seleccionados por el algoritmo de predicción. Por último, el tercero envía los datos de las predicciones a Supercollider y utiliza esa información para modificar en tiempo real los parámetros de varios sintetizadores o \emph{ugens}. En este sentido, el tipo de interacción de SEALI se encuentra en dos esquemas: la sonificación, donde los datos de clasificaciones y predicciones son aplicados para cumplir con diferentes funciones booleanas y mapeados para modificar los estados internos de diferentes sintetizadores, y el esquema de reproducción de archivos de audio de diferentes bases de datos. Este último esquema responde de manera iterativa al siguiente planteamiento: dada una serie de datos de entrada, qué es lo que sigue a continuación. Estos algoritmos fueron implementados bajo una arquitectura cliente/servidor mediante Python, Supercollider y TensorFlow Serving, usando librerías como tensorflow, keras, scikit-learn, essencia, scmir, pydub, pyaudio, pythonosc, toolz, request, entre otras. 
