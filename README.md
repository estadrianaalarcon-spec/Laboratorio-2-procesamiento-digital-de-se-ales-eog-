# Laboratorio 2 procesamiento digital de señales eog

Docente: Carolina Corredor

Participantes:

Adriana Valentina Alarcon Ramirez 

Liseth Yuliana Clavijo Mesa

# Introducción

El procesamiento digital de señales es una herramienta fundamental en la ingeniería biomédica, ya que permite analizar, transformar y extraer información relevante de señales en diferentes dominios. Dentro del campo del procesamiento de señales, la convolución se utiliza para determinar la respuesta de un sistema discreto a una señal de entrada, siendo esencial para comprender el comportamiento de filtros y sistemas lineales invariantes en el tiempo. Por otro lado, la correlación constituye un método de comparación entre señales, ya que mide el grado de similitud y es ampliamente empleada en detección de patrones, sincronización y análisis de señales biomédicas. Finalmente, la transformada de Fourier brinda la posibilidad de estudiar las señales en el dominio de la frecuencia, facilitando la identificación de sus componentes espectrales y su caracterización estadística.

Esta práctica de laboratorio busca integrar estos tres conceptos aplicados. Para ello, se realiza el cálculo de convolución tanto manual como mediante Python, se analizará la correlación cruzada entre señales sinusoidales y se estudiará una señal biológica a partir de su muestreo y representación espectral. De esta manera, se fortalece la comprensión teórica y práctica de las principales herramientas del procesamiento digital de señales, resaltando su relevancia en aplicaciones de la ingeniería biomédica y áreas afines.

# Marco teorico 

El procesamiento digital de señales se centra en la representación, análisis y manipulación de señales mediante técnicas matemáticas implementadas en computadoras y sistemas digitales, entre sus herramientas principales se encuentran la convolución, la correlación y la transformada de Fourier, que permiten comprender y caracterizar el comportamiento de señales y sistemas.

## Convolución 


La convolución es una operación matemática que combina dos señales o funciones para obtener una tercera señal que describe cómo un sistema responde a una entrada.

Permite determinar la respuesta de un sistema a una señal de entrada, en sistemas discretos, esta operación combina una señal de entrada con la respuesta al impulso del sistema, generando como resultado la señal de salida, la convolución describe cómo cada valor de la señal de entrada influye en el comportamiento del sistema a lo largo del tiempo, este procedimiento es fundamental para el análisis de sistemas lineales invariantes en el tiempo, así como para el diseño y estudio de filtros digitales utilizados en el procesamiento de señales biomédicas.

<img width="294" height="93" alt="image" src="https://github.com/user-attachments/assets/f73837b5-5aa9-483a-9566-bddc50d541ad" />

## Correlación

La correlación es una operación matemática utilizada en el procesamiento de señales que permite medir el grado de similitud entre dos señales en función de un desplazamiento entre ellas, la correlación cruzada entre dos señales discretas x[n] y y[n] se define como:

<img width="313" height="78" alt="image" src="https://github.com/user-attachments/assets/81c23f59-b94f-43ab-81ab-cd4e54b811ee" />


A través de este proceso se compara una señal con otra para determinar qué tan parecidas son y en qué posición presentan mayor coincidencia.

##  Transformada de Fourier

La transformada de Fourier es una herramienta matemática utilizada en el procesamiento de señales que permite representar una señal en el dominio de la frecuencia, mediante esta transformación, una señal que originalmente se describe en función del tiempo puede expresarse como la suma de diferentes componentes sinusoidales de distintas frecuencias, amplitudes y fases, la transformada de Fourier facilita el análisis de las características espectrales de una señal y permite identificar las frecuencias que la componen, siendo una herramienta fundamental en el estudio, filtrado y procesamiento de señales biomédicas.


<img width="259" height="98" alt="image" src="https://github.com/user-attachments/assets/b7905e8b-4bb3-44e7-ad76-ab9e60205c70" />

La Transformada Rápida de Fourier (FFT) es un algoritmo utilizado para calcular la Transformada Discreta de Fourier (DFT) de una señal, su principal ventaja es que reduce significativamente el número de operaciones necesarias para obtener el espectro de frecuencias de una señal, permitiendo realizar el análisis de manera mucho más rápida que con el cálculo directo de la DFT.

# Objetivos 

Reconocer la importancia de la aplicación de herramientas
matemáticas como la convolución y correlación en el área de procesamiento de
señales.

## Objetivos Específicos

-Comprender la convolución como una operación que permite obtener la respuesta de un sistema discreto ante una entrada determinada.

-Analizar la correlación como medida de similitud entre dos señales.

  
-Aplicar la Transformada de Fourier como herramienta de análisis en el
dominio de la frecuencia. 

# Procedimientos y resultados
## PARTE A
Teniendo el sistema ℎ[𝑛] = {𝑐𝑎𝑑𝑎 𝑑í𝑔𝑖𝑡𝑜 𝑑𝑒 𝑠𝑢 𝑐ó𝑑𝑖𝑔𝑜} (ej: ℎ[𝑛] = {5,6,0,0,1,4,6})
y la señal 𝑥[𝑛] ={𝑐𝑎𝑑𝑎 𝑑í𝑔𝑖𝑡𝑜 𝑑𝑒 𝑠𝑢 𝑐é𝑑𝑢𝑙𝑎} (ej: 𝑥[𝑛] = {1,0,2,1,4,5,4,8,1,9}):


1. Encuentre la señal 𝑦[𝑛] resultante de la convolución usando sumatorias (a
mano)
2. Encuentre la representación gráfica y secuencial (a mano).

   
### Adriana 
ℎ[𝑛]= {5,6,0,0,8,5,0}

![capture_temp](https://github.com/user-attachments/assets/181fce05-2f77-4f63-9b33-9dcf20f8b30b)


𝑥[𝑛]= {1,0,7,6,2,4,2,2,6,3}

![capture_temp](https://github.com/user-attachments/assets/f06ae621-53bd-4495-83b7-fae9c2bcb9b0)



### Yuliana 
ℎ[𝑛]= {5,6,0,0,8,6,2}

𝑥[𝑛]= {1,0,7,3,5,9,9,5,7,0}


3. Encuentre la señal 𝑦[𝑛] resultante de la convolución usando Python.

   
4. Encuentre la representación gráfica y secuencial usando Python.








