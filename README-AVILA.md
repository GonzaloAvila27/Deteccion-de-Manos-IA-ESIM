## 3 -Explicar cómo está compuesto el proyecto, los requerimientos de instalación, que
## conforman las librerías que utiliza y si utiliza algún modelo neuronal.


a. Este proyecto está diseñado para realizar un seguimiento y detección de la posición y dirección de la mano en tiempo real utilizando la cámara web y landmarks especificos. Esta basado en detección de manos con Mediapipe y visualización con OpenCV, sin necesidad de entrenamiento adicional o de un modelo neuronal explícito. 

b. Requerimientos de Instalación:
- Numpy 'pip install numpy'
- OpenCV 'pip install opencv-python'
- Mediapipe 'pip install mediapipe'
- TensorFlow 'pip install tensorflow'

### c. Librerías Utilizadas
OpenCV: Para capturar el video, mostrar ventanas en tiempo real y dibujar puntos y líneas en las imágenes.
Mediapipe: Para detectar y obtener los puntos de referencia de la mano.
NumPy: Para la manipulación de matrices de imágenes. 
TensorFlow: se emplea solo para silenciar advertencias de registros.

### d. ¿Utiliza Algún Modelo Neuronal?
El proyecto no usa ningun modelo neuronal (entrenado en este código) Mediapipe si utiliza modelos preentrenados internamente para la detección de puntos de referencia de la mano, pero esta oculto dentro de la biblioteca.

### 4- Link bitly: 


### 5- Indicar si el proyecto podría utilizar la GPU, ¿sí?, ¿no?. justificando su respuesta.

En el proyecto el uso de la GPU es posible y puede ser beneficioso, para mejorar la eficiencia en el procesamiento de video LIVE y el análisis de puntos de referencia.

 Mediapipe (Landmarks de la Mano): es la biblioteca que calcula los puntos de referencia(landmarks). y solo ofrece aceleración por GPU en dispositivos móviles (Android, iOS). En entornos de escritorio, utiliza principalmente la CPU.

 TensorFlow: Aunque tiene compatibilidad con la GPU, en este código no se utiliza para procesamiento, mas si se expandiera, se podria utilizar tensor con GPU para hacer una red neuronal de detección y clasificación avanzada. 

 OpenCV (cv2): tiene soporte para la aceleración por GPU en operaciones específicas, pero en el código, no están configuradas explícitamente para usar la GPU. Es posible modificarlo para aprovechar una versión de OpenCV con CUDA y mejorar el rendimiento.

Conclusión: En su forma actual, el proyecto NO utiliza la GPU, pero, se puede optimizar.