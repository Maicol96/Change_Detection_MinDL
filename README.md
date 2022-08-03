# change-detection_DL
## Repositorio para el proceso de detección de cambios de minería y deforestación basado en algoritmos de Deep Learning

El proceso consiste en una metodologia basada en arquitecturas de Deep Learning para la deteccion de cambios en zonas de mineria en Colombia. Para ello se plantean dos esquemas para la generación de cambios, uno basado en la comparación post-clasificación en el cual se evalúan dos arquitecturas de redes neuronales convolucionales (CNN): U-Net y FPN (Feature Pyramidal Network) para la clasificación de áreas de minería a lo largo de series de tiempo, para ello se generaron y entrenaron diferentes modelos con el fin de seleccionar el más adecuado para dicho proceso y posteriormente realizar la diferencia entre los periodos de la serie; y un segundo esquema basado en la detección de cambios directa en el que se evaluó una red U-Net modificada para detectar cambios a partir de pares de imágenes, para ello también se entrenaron diferentes modelos seleccionando el más adecuado para la detección de cambios por cada periodo de la serie de tiempo, obteniendo un mapa de cambios por cada esquema. El esquema más adecuado fue el numero 2 (Detección de cambios directa), los resultados obtenidos y los diferentes procesos empleados permitieron plantear un marco metodológico para la detección, delimitación y clasificación de cambios sobre este tipo de coberturas.

![image](https://user-images.githubusercontent.com/16407959/141313155-15a16d7e-6238-4254-9014-1d174d974884.png)

Figura 1: Proceso obtención de cambios Esquema 1: comparación post - clasificación.

![image](https://user-images.githubusercontent.com/16407959/141313188-980bc1b0-1f09-4e24-b9c1-8574b9e8bc66.png)

Figura 2: Proceso obtención de cambios Esquema 2: detección directa.


La zona de estudio para la cobertura de minería corresponde a un área de 327.16 km2 ubicada en 5 diferentes municipios pertenecientes al departamento de la Guajira, en esta zona hay presencia de minería a cielo abierto a gran escala la cual hace parte de la Mina del Cerrejón, la serie de tiempo de imágenes satelitales Planet de esta zona se compone de 8 imágenes ubicadas entre 2017 y 2019. 

La ejecución de todo el proceso se encuentra en su mayoría enmarcado bajo una arquitectura en la nube, haciendo uso de los recursos gratuitos provistos por Google Earth Engine, Google Colab y Google Cloud y toda la suite de herramientas que componente estos entornos y que fueron de utilidad para la automatización, entrenamiento de los modelos, almacenamiento y ejecución de las diferentes etapas que componen la metodología planteada).

## Organizacion Carpetas
- **minería**: Códigos asociados al proceso de creación de muestras para los modelos, y el proceso de entrenamiento de los modelos bajo el esquema 1: U-Net y FPN para la zona de minería.
- **mineria_M2**: Códigos asociados al proceso de creación de muestras para los modelos, y el proceso de entrenamiento de los modelos bajo el esquema 2: U-Net Modificada para la zona de minería.
- **Validación**: Códigos para el cálculo de las medidas de exactitud para las segmentaciones obtenidas bajo el esquema 1, y los cambios obtenidos bajo los dos esquemas para las dos zonas de estudio.

En el siguiente enlace se encuentran los datos de entrenamiento obtenidos por cada esquema según los bloques obtenidos para cada zona de estudio [Data_Change_Detecion-DL](https://drive.google.com/drive/folders/1o0O-Gturw0D1yuOFpbkMmHFKUXp6rQsR?usp=sharing)
