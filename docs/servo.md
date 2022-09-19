# <FONT COLOR=#8B008B>3.7. A06-Servomotores</font>
## <FONT COLOR=#007575>Teoría</font>
Un servomotor o abreviado servo es un motor especial que puede posicionar su eje en un ángulo determinado y lo puede mantener en esta posición. Los servos estándar suelen girar 180º, pero es habitual encontrar servos que giran 90º y otros 360º, que son los conocidos como servos de rotación continua. En el interior del mismo están ubicados tanto la electrónica de control como los engranajes reductores que a su vez pueden llevar o no topes físicos que marquen el ángulo de giro. Para su funcionamiento sólo necesita alimentación ser alimentados (conexiones GND y VCC o 5V) y una señal de control.

Los servomotores son en realidad motores de corriente continua a los que se les ha añadido una reductora, para que giren más despacio y con más fuerza, y un controlador electrónico que permite hacer que gire un determinado ángulo. Además, el servo en todo momento sabe en qué posición está, aunque se apague o reinicie. Esto significa que si a un servo que hemos movido a un determinado punto, lo hemos dejado sin alimentación y al alimentarlo de nuevo le indicamos que gire 90º, no va a girar 90º sino que se va a dirigir a su posición de 90º que tiene memorizada internamente.

En la Figura 3.7.1 vemos el interior de un servo esquematizado.

<center>

![Interior de un servo 9g](../img/3_retos/3_7/F3_7_1.png)

*Figura 3.7.1. Interior de un servo 9g*

</center>

Su aspecto real lo vemos en la Figura 3.7.2 donde también se aprecian las palas y tornilleria que lo acompañan.

<center>

![Aspecto real servo 9g](../img/3_retos/3_7/F3_7_2.png)

*Figura 3.7.2. Aspecto real servo 9g*

</center>

Veamos su principio básico de funcionamiento: La electrónica de control del servomotor tiene un circuito de referencia incorporado que emite la señal de referencia, que es un ciclo de 20 ms con un ancho de pulso de 1,5 ms. Se compara la tensión de control recibida con la de referencia y se genera una diferencia de tensión. El circuito de control en la placa decidirá la dirección de rotación en consecuencia y accionará el motor. El sistema de engranajes o reductora convierten el giro del motor en un par de fuerza a través del eje. El sensor detecta que se ha alcanzado la posición enviada  de acuerdo con la señal de retroalimentación. Cuando la diferencia de tensión existe el motor gira y cuando la diferencia se reduce a cero, el motor se detiene. Normalmente, el ángulo de rotación es de 0 a 180 grados.

El servomotor viene con un conector hembra de tres pines para tres cables de conexión, que se distinguen por los colores marrón, rojo y naranja (diferentes marcas pueden tener diferentes colores).

El ángulo de rotación del servomotor se controla regulando el ciclo de trabajo de la señal PWM cuyo estándar es de 20 ms (50 Hz).

Hay que tener mucho cuidado de posicionar el conector de los servos en los tres pines macho de la shield en el orden correcto (el conector es reversible) o seguramente romperemos algo de manera irremediable.

Existe un tipo especial de servomotor que permite la rotación continua. En algunos casos se trata de servomotores “trucados” de forma que se modifican para permitir la rotación continua quitando los topes mecánicos y se sustituye el potenciómetro por un divisor de tensión con dos resistencia iguales (en algunos casos no se ponen resistencias y se bloquea el potenciómetro para que no gire dejándolo justo en su punto central). Este tipo de modificación la podemos realizar nosotros (en la web existen multitud de tutoriales) o también podemos comprar un servomotor de rotación continua listo para funcionar sin tener que hacer ningún tipo de bricolaje. 

En el apartado de bloques de programación, se encuentra en "Motor / Servo" y en la Figura 3.7.3 vemos los bloques disponibles.

<center>

![Bloques para servos](../img/3_retos/3_7/F3_7_3.png)

*Figura 3.7.3. Bloques para servos*

</center>

Para controlar el servomotor, indicamos los grados de rotación (Ángulo de giro) que queremos y el tiempo de retardo, o tiempo que tarda en ir de una posición a otra.

El control de un servomotor de rotación continua se realiza de igual manera, pero su reacción es diferente.

Los bloques Servo-Oscilador nos permiten de una forma sencilla hacer que el servo repita una secuencia de movimientos u oscilaciones de forma indefinida. Aunque no vamos a aplicarlo en el caso de ma Smart home, un ejemplo típico puede ser el que vemos en la Figura 3.7.4, donde el servo oscila entre 0 y 90º en periodos de dos segundos.

<center>

![Oscilación con servo](../img/3_retos/3_7/F3_7_4.png)

*Figura 3.7.4. Oscilación con servo*

</center>

El bloque Servo-I2C (PCA9685) es simplemente un bloque para manejar la tarjeta controladora para 16 servos PCA9685 utilizando el bus I2C.

## <FONT COLOR=#007575>**Listas**</font>
Las listas de datos nos permiten almacenar un listado de valores y acceder a ellos por su posición en la lista. Las listas pueden ser de tipo numéricas o de texto, como vemos en la imagen siguiente:

<center>

| Tipos de listas en ArduinoBlocks |
|:|
|![Tipos de listas en ArduinoBlocks](../img/3_retos/3_7/tipos-listas.png)|

</center>

En la animación siguiente vemos el proceso de creación de una lista numérica y los elementos que se crean con la misma.

<center>

![Creación de una lista numérica](../img/3_retos/3_7/crear.gif)

</center>

Los bloques que se crean nos permiten asignarle valores, saber el número de elementos que tiene una lista, obtener el valor de una posición de la lista o cambiar el valor de un elemento de la lista.

De forma muy similar se pueden crear y trabajar con lista de textos.

### <FONT COLOR=#AA0000>Actividad A06_1</font>
Esta primera actividad va a consistir en posicionar el servo de la ventana (pin 10) en posiciones prefijadas en una lista. La solución la tenemos disponible en [Smart-home-A06_1](http://www.arduinoblocks.com/web/project/914702).

<center>

![Solución A06_1](../img/3_retos/3_7/F3_7_5.png)

*Figura 3.7.5. Solución A06_1*

</center>

### <FONT COLOR=#AA0000>Actividad A06_2</font>
En esta actividad controlaremos la posición angular de la puerta mediante el servomotor al cual está unida. Este servomotor está conectado en el pin D9. La solución la tenemos disponible en [Smart-home-A06_2](http://www.arduinoblocks.com/web/project/914730).

<center>

![Solución A06_2](../img/3_retos/3_7/F3_7_6.png)

*Figura 3.7.6. Solución A06_2*

</center>
