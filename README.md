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


convolución h[n] * x[n]

![capture_temp](https://github.com/user-attachments/assets/d8eaddb2-01da-46cd-9a8f-87ef5543fe27)




![capture_temp](https://github.com/user-attachments/assets/b056d112-3a50-4774-a014-e6451cd7088e)




### Yuliana 
ℎ[𝑛]= {5,6,0,0,8,6,2}

![capture_temp](https://github.com/user-attachments/assets/087a53a0-9f81-4dcb-aa19-7e6351274e0c)


𝑥[𝑛]= {1,0,7,3,5,9,9,5,7,0}

![capture_temp](https://github.com/user-attachments/assets/679807bf-7484-4e67-b6f8-f3ed8feabbea)

convolución h[n] * x[n]

![capture_temp](https://github.com/user-attachments/assets/ddf846e2-91ae-46ce-a14b-4d1ece923c7c)


![capture_temp](https://github.com/user-attachments/assets/ee28a640-b368-444d-bbc8-d02ec2563c02)



3. Encuentre la señal 𝑦[𝑛] resultante de la convolución usando Python.

   
4. Encuentre la representación gráfica y secuencial usando Python.


Se definió la señal discreta h(n) y x(n) y se representaron mediante la función plt.stem, que permite graficar valores discretos en forma de impulsos. En la gráfica se observa la variación de la amplitud de la señal en función del índice n, añadiendo título y etiquetas a los ejes para una mejor interpretación

### Adriana 

```python
#Señal h(n) adriana
x = [0, 1, 2, 3, 4, 5, 6]
h = [5, 6, 0, 0, 8, 5, 0]

plt.stem(x,h)
plt.title('Grafica señal h(n)', fontsize=14, fontweight='bold')
plt.xlabel('Índice discreto n', fontsize=12)
plt.ylabel('Amplitud de h[n]', fontsize=12)
Se grafica la señal de salida  𝑦[𝑛]
```

<img width="720" height="578" alt="image" src="https://github.com/user-attachments/assets/b32b0a81-c4c2-4e09-b282-793dfb8b0f2a" />


```python
#Señal x(n) Adriana 
x = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
h = [1, 0, 7, 6, 2, 4, 2, 2, 6, 3]

plt.stem(x,h)
plt.title('Grafica señal x(n)', fontsize=14, fontweight='bold')
plt.xlabel('Índice discreto n', fontsize=12)
plt.ylabel('Amplitud de x[n]', fontsize=12)
```

<img width="736" height="572" alt="image" src="https://github.com/user-attachments/assets/7e0cc856-3891-4c85-8a2b-9da2a174637e" />


Convolución: Para ello se utiliza la función np.convolve(x, h), la cual genera una nueva secuencia y[n] que representa el resultado de combinar ambas señales.
Posteriormente, con matplotlib, se grafica el resultado en un diagrama de tallo (stem plot), el cual es adecuado para señales discretas.

```python
import numpy as np
import matplotlib.pyplot as plt
#Convolucion Adriana
x = np.array([1,0,7,6,2,4,2,2,6,3])
h = np.array([5,6,0,0,8,5,0])
y=np.convolve(x,h)
plt.figure(figsize=(10,4))
plt.stem(y)
plt.title('Convolución de las señales x[n] y h[n]', fontsize=14, fontweight='bold')
plt.xlabel('Índice discreto n', fontsize=12)
plt.ylabel('Amplitud de y[n]', fontsize=12)
plt.grid(True)
plt.show()
```

<img width="722" height="342" alt="image" src="https://github.com/user-attachments/assets/66eef21b-f2b9-4791-a1f6-5eef5a199d84" />

### Yuliana 


Para la convolución de las señales h(n) * x(n) de Yuliana se realiza el mismo proceso y codigo.

```python
#Señal h(n) adriana
x = [0, 1, 2, 3, 4, 5, 6]
h = [5, 6, 0, 0, 8, 6, 2]

plt.stem(x,h)
plt.title('Grafica señal h(n)', fontsize=14, fontweight='bold')
plt.xlabel('Índice discreto n', fontsize=12)
plt.ylabel('Amplitud de h[n]', fontsize=12)
Se grafica la señal de salida  𝑦[𝑛]
```

<img width="715" height="558" alt="image" src="https://github.com/user-attachments/assets/895bcd31-cba5-4372-a3a7-03ab92d6bea3" />

```python
#Señal x(n) Adriana 
x = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
h = [1, 0, 7, 3, 5, 9, 9, 5, 7, 0]

plt.stem(x,h)
plt.title('Grafica señal x(n)', fontsize=14, fontweight='bold')
plt.xlabel('Índice discreto n', fontsize=12)
plt.ylabel('Amplitud de x[n]', fontsize=12)
```
<img width="713" height="557" alt="image" src="https://github.com/user-attachments/assets/fcc2eab7-f728-4d40-9015-d2ed7ae35182" />

```python
import numpy as np
import matplotlib.pyplot as plt
# convolución señal Yuliana 

x = np.array([1,0,7,3,5,9,9,5,7,0])
h = np.array([5,6,0,0,8,6,2])
y=np.convolve(x,h)
plt.figure(figsize=(10,4))
plt.stem(y)
plt.title('Convolución de las señales x[n] y h[n]', fontsize=14, fontweight='bold')
plt.xlabel('Índice discreto n', fontsize=12)
plt.ylabel('Amplitud de y[n]', fontsize=12)
plt.grid(True)
plt.show()
```

<img width="724" height="342" alt="image" src="https://github.com/user-attachments/assets/b0c0cbdc-c714-4a21-af6b-6d13fc333800" />

## PARTE B 

## PARTE C

A partir de la señal adquirida mediante el sistema de adquisición de datos, se determio el periodo de muestreo Ts a partir de la diferencia entre muestras consecutivas de tiempo, posterior a esto se calcula la frecuencia de muestres Fs como Fs=1/Ts y  la frecuancia de Nyquist que corresponde a FN= Fs/2, la frecuencia de muestreo utilizada para esta práctica sera cuatro veces la frecuencia de Nyquist fs​=4fN esto garantiza que la seal sea muestreada con suficiente resolución temporal, evitando pérdidas de infromación en el proceso de digitalización.

```python

import pandas as pd
data = pd.read_csv("Medicion_DAQ_27.csv")
data.head()
import numpy as np
#columna de tiempo
t=data["Tiempo (s)"]
#Ts
Ts=np.mean(np.diff(t))
print("Periodo de muestreo Ts=",Ts)
fs=1/Ts
print("Frecuencia de muestreo fs=",fs,"Hz")
f_nyquist=fs/2
print("Frecuencia de Nyquist=",f_nyquist,"Hz")

import matplotlib.pyplot as plt
t=data["Tiempo (s)"]
plt.figure()
plt.plot(t,x)
plt.title("Señal eog medida")
plt.xlabel("Tiempo (s)")
plt.ylabel("Voltaje (V)")
plt.show()
```

<img width="714" height="554" alt="image" src="https://github.com/user-attachments/assets/edde8e9b-b778-4ec7-b2ab-5d6288f762ca" />

Caracterización de la señal en el dominio del tiempo, para describir el comportamiento de la señal en el dominio temporal se calcularon los principales estadisticos descriptivos: media, mediana, desviación estandar, valor máximo y valor mínimo. Estos parametros permiten caracterizar la distribución de amplitudes y la variabilidad de la señal biológica analizada en este caso EOG.

```phyton

import numpy as np
import pandas as pd
data = pd.read_csv("Medicion_DAQ_27.csv")
x=data["Voltaje (V)"]
# Estadísticos
media=np.mean(x)
mediana=np.median(x)
desviacion=np.std(x)
maximo=np.max(x)
minimo=np.min(x)

print("Media=",media)
print("Mediana=",mediana)
print("Desviación estándar=",desviacion)
print("Máximo=",maximo)
print("Mínimo=",minimo)

```

La señal analizada corresponde a una señal aleatoria y aperiódica, ya que proviene de una medición biológica y no presenta repetición exacta en el tiempo. Además, es digital, puesto que fue adquirida mediante un sistema de adquisición de datos y se encuentra representada mediante muestras discretas.

Análisis en el dominio de la frecuencia
Para analizar el contenido frecuencial de la señal se aplicó la Transformada Rápida de Fourier (FFT), esta herramienta permite transformar la señal desde el dominio del tiempo al dominio de la frecuencia, revelando las componentes frecuenciales presentes en la señal.

A partir de la FFT se obtuvieron:
Espectro de magnitud de la señal, que muestra las frecuencias presentes, densidad espectral de potencia (PSD) que describe cómo se distribuye la energía de la señal en función de la frecuencia.

La PSD se representó en escala logarítmica (dB) con el fin de visualizar con mayor claridad tanto las componentes de alta energía como aquellas de menor amplitud.

Adicionalmente se calcularon estadísticos espectrales, tales como:

Frecuencia media, que representa el centro de gravedad del espectro.

Frecuencia mediana, que divide la distribución de energía espectral en dos partes iguales.

Desviación estándar en frecuencia, que indica la dispersión de las componentes frecuenciales.

Finalmente, se representó un histograma de la potencia espectral en escala logarítmica, lo cual permite observar la distribución de la energía de las diferentes componentes frecuenciales presentes en la señal.



​


















