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
- **Bibliotecas de Python:** `numpy`,`matplotlib.pyplot`,`scipy`,`sklearn`.

## Análisis Espectral
Permite descomponer una señal en sus componentes de frecuencia, se usa para caracterizar las distintas fuentes sonoras y buscar patrones que faciliten su separación. Se usa tranformada rápida de Fourier (FFT) porque como su nombre lo dice, el algoritmo es más rápido y eficiente, lo que nos permite comparar de cada audio su espectro para identificar que sonidos provienen de qué fuente.

![image](https://github.com/user-attachments/assets/e19c8a8e-9c12-4e18-9bc4-0ec914194f4c)
### *Figura 1: Lineas de código para realizar el análisis espectral.*

![WhatsApp Image 2025-03-03 at 9 16 58 PM](https://github.com/user-attachments/assets/b32134c0-9ddc-46e3-904b-d54476306ec1)
### *Figura 2: Espectro de frecuencia de cada audio.*


## Métodos de separación de fuentes 
- **Análisis de componentes independientes (ICA)**: Es una técnica estadística que se utiliza para separar señales mezcladas en sus componentes originales, suponiendo que estas son estadisticamente independientes entre sí.
- **Beamforming**:Utiliza matrices de microfonos para enfocar la captación de sonido en una dirección específica, incrementando el SNR de la fuente deseada y atenuando fuentes no deseadas.
-  **Descomposición en valores singulares (SVD)**: Se utiliza para analizar matrices de datos y encontrar patrones dominantes, pudiendo ser aplicada para separar fuentes de audio.

## Resultados 
![WhatsApp Image 2025-03-03 at 9 15 56 PM](https://github.com/user-attachments/assets/9795c18b-3c34-47cf-a6f7-64472b7aca28)
Figura codigo y calculos 


![WhatsApp Image 2025-03-03 at 9 16 58 PM (1)](https://github.com/user-attachments/assets/e8d09631-99e1-4312-b20f-c37f45f4f6d1)

![WhatsApp Image 2025-03-03 at 9 16 58 PM (2)](https://github.com/user-attachments/assets/95280872-d3b8-4736-b008-80bf4fb69c23)
![WhatsApp Image 2025-03-03 at 9 18 46 PM](https://github.com/user-attachments/assets/c771d36a-9499-460d-8c21-fcadf576521e)

## Conclusiones

-La tecnica de analisis de componentes independientes (ICA) permitio descomponer las señales mezcladas en tres componentes separados. Sin embargo las señales resultantes no coinciden exactamente con las señales originales, sino con aproximaciónes independientees
-Los valores negativos de la Relación Señal-Ruido (SNR) indican que las señales separadas difieren significamente de los originales, lo que es esperablem dado que ICA separa las fuentes, pero no necesariamente en su forma pura. Esto sugiere que las señales separadas pueden contener combinaciones de ruido y componentes residuales  de otras señales
-La Transformada Rápida de Fourier (FFT) permitió visualizar las frecuencias dominantes de cada señal, permite  identificar si las señales tienen componentes espectrales bien definidos que podrían aprovecharse para mejorar la separación.



