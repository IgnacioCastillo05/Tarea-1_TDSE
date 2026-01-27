## Tarea-1_TDSE
## Trabajo de TDSE sobre regresión lineal

## Cuaderno #1 - Regresión lineal con una característica (Vectorizado y No Vectorizado)
- Model and loss:
El nuevo dataset dado nos da que la función de costo (J(w,b)) es de 117.69675 L^2. A este valor de la función de costo, como está definido como "error promedio al cuadrado", se toma la raíz cuadrada de lo obtenido, que sería aproximadamente 10.85. Esto representa que en promedio tus predicciones están a ~10.85 unidades de los valores reales, lo cual está mal debido a que los valores van de 0.15 a 35.0.

- Cost surface:
El mínimo de la superficie de costo representa los valores óptimos de los parámetros que mejor ajustan nuestros datos de luminosidad estelar. 

El mínimo corresponde a los valores de w y b que minimizan el error cuadrático medio entre nuestras predicciones (L_hat = w*M + b) y las observaciones reales de luminosidad (L).

w_óptimo: La tasa a la cual la luminosidad estelar aumenta por unidad de masa estelar (la pendiente de la relación masa-luminosidad)
b_óptimo: El intercepto teórico de luminosidad (aunque físicamente no realista en M=0)
J_mínimo: El error residual que no puede ser eliminado, representando ruido en las mediciones o la limitación inherente de un modelo lineal para esta relación

El descenso por gradiente se mueve iterativamente desde cualquier punto inicial en esta superficie hacia el mínimo, siguiendo la dirección de mayor descenso. La forma convexa (tipo cuenco) de la superficie de costo garantiza que el descenso por gradiente convergirá al mínimo global.

La superficie exhibe una estructura claramente convexa con un único mínimo global, lo que confirma que nuestro problema de regresión lineal está bien planteado y que el descenso por gradiente encontrará confiablemente la solución óptima sin importar la inicialización.

## No Vectorizado:
Continuando con lo visto en clase, en primer lugar se toma el dataset dado y se hacen los respectivos cálculos de la gradiente descendiente sin vectorizarlo. Se utilizaron de valores de alpha a 0.01, 0.05 y 0.1

0.01 con 1000 iteraciones:
![alt text](fotos/image.png)
![alt text](fotos/image-1.png)

0.05 con 1000 iteraciones:
![alt text](fotos/image-2.png)
![alt text](fotos/image-3.png)

0.1 con 1000 iteraciones:
![alt text](fotos/image-4.png)
![alt text](fotos/image-5.png)

## Vectorizado:

0.01 con 2000 iteraciones:
![alt text](fotos/image-6.png)
![alt text](fotos/image-7.png)

0.05 con 2000 iteraciones:
![alt text](fotos/image-8.png)
![alt text](fotos/image-9.png)

0.1 con 2000 iteraciones:
![alt text](fotos/image-10.png)
![alt text](fotos/image-11.png)
