# Cóctel Lab-3
Este laboratorio tiene como objetivo aplicar el analisis de frecuencia de las señales de voz en un conjunto de señales que están mezcladas con el fin de adquirir una sola señal entre varias.El código esta implentado en Python y utiliza bibliotecas como `wfdb`, `numpy`,`matplotlib` y `scipy.
## Tabla de Contenido
1.[Introducción](#introducción)
2.[Requisitos](#requisitos)
3.[Análisis Espectral](#Análisis_Espectral)
4.[Métodos de separación de fuentes](#Métodos_de_separación_de_fuentes)
5.[Resultados](#Resultados)
6.[Conclusión](#conclusión)

## Introducción
El laboratorio recibe el nombre de Coctel haciendo referencia a el problema de **fiesta de cóctel** que consiste en un sistema para concentrarse en una sola fuente sonora mientras filtra las demás en un entorno con múltiples emisores de sonido. La resolución de este problema permite mejorar la voz, el reconocimiento del habla y la cancelación del ruido. Para recrear este problema se realiza lo siguiente:

1. Los integrantes del grupo van a grabarse con una aplicación de grabadora de voz que puede venir por defecto en los dispositivos móviles. Preferiblemente con el mismo sistema operativo (Android, iOS).
2. Deben estar a cierta distancia de los dispositivos los cuales deben estar ubicados de manera diferente, es decir, apuntando en diferentes direcciones, con el fin de que la grabadora capte más la voz que esta en esa dirección.
3. Cada integrante debe hablar durante cierto tiempo y de manera simultánea, como si estuviera en una fiesta de cocteles.
4. Por último, una vez se graban las n voces en un determinado tiempo, se procede a calcular el SNR. Si el SNR de alguna de las señales de audio es bajo, es necesario repetir la medición.

## Requisitos 
- **Phyton** Instalado en tu sistema.
- **Spyder** (Puedes instalarlo como parte de [Anaconda](https://www.anaconda.com/)).
- **Bibliotecas de Python:** `numpy`,`matplotlib`,`wfdb`.

## Análisis Espectral
Permite descomponer una señal en sus componentes de frecuencia, se usa para caracterizar las distintas fuentes sonoras y buscar patrones que faciliten su separación

## Métodos de separación de fuentes 
- **Análisis de componentes independientes (ICA)**: Es una técnica estadística que se utiliza para separar señales mezcladas en sus componentes originales, suponiendo que estas son estadisticamente independientes entre sí.
- **Beamforming**:Utiliza matrices de microfonos para enfocar la captación de sonido en una dirección específica, incrementando el SNR de la fuente desead y atenuando fuentes no deseadas
-  **Descomposición en valores singulares (SVD)**: Se utiliza para analizar matrices de datos y encontrar patrones dominantes, pudiendo ser aplicada para separar fuentes de audio


