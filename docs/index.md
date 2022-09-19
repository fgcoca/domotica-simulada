# <FONT COLOR=#8B008B>1. Domótica</font>
Según la [Wikipedia](https://es.wikipedia.org/wiki/Dom%C3%B3tica) *"se llama domótica a los sistemas capaces de automatizar una vivienda o edificación de cualquier tipo, aportando servicios de gestión energética, seguridad, bienestar y comunicación, y que pueden estar integrados por medio de redes interiores y exteriores de comunicación, cableadas o inalámbricas, y cuyo control goza de cierta ubicuidad, desde dentro y fuera del hogar. Se podría definir como la integración de la tecnología en el diseño inteligente de un recinto cerrado."*

*El término domótica viene de la unión de las palabras domus (casa en latín) y autónomo (del griego: αὐτόνομος; “que se gobierna a sí mismo”).*

Existen multitud de tecnologías y protocolos que definen todo lo relacionado con domótica.

El término **domótica** se usa para referirse a viviendas, cuando aplicamos el concepto a inmuebles se **inmótica** y cuando lo aplicamos a ciudades **urbótica**. Podemos resumir los conceptos de la forma siguiente:

* **Domótica**. Conjunto de tecnologías aplicadas al control y la automatización inteligente de la vivienda, que permite una gestión eficiente del uso de la energía, aporta seguridad, confort y comunicación entre el usuario y el sistema.

* **Inmótica**. Conjunto de tecnologías aplicadas al control y la automatización inteligente de edificios no destinados a vivienda, como hoteles, centros comerciales, escuelas, universidades, hospitales y edificios terciarios, permitiendo una gestión eficiente del uso de la energía, además de aportar seguridad, confort, y comunicación entre el usuario y el sistema.

* **Urbótica**. Conjunto de servicios e instalaciones públicas urbanas que se encuentran automatizadas con el fin de mejorar la gestión energética, la seguridad, el bienestar, el confort y las comunicaciones de todos los usuarios de estos servicios públicos.

A continuación vemos un listado de términos que escucharemos habitualmente cuando hablamos de domótica:

* Interruptor crepuscular
* Actuador
* Automatización
* Detector
* Estación meteorológica automática
* Hogar digital
* HomeOS. Sistema operativo para domótica desarrollado por Microsoft
* Ingeniería mecatrónica
* Inmótica
* Internet de las Cosas (IoT)
* Interruptor
* Reconocimiento de gestos
* Red doméstica
* Red eléctrica inteligente
* Robot doméstico
* Tarjeta SIM
* Teleasistencia
* Telemedicina
* Urbótica
* Wi-Fi Direct
* CSI (bus serie). Bus serie para cámaras

De estas modalidades aquí solamente hablaremos de domótica y en cuanto a aplicación real a simulaciones con elementos pensados para la enseñanza.

## <FONT COLOR=#007575>**1.1. Domótica real**</font>
Cuando hablamos de domótica nos referimos a crear casas inteligentes, lo que las hará mas seguras en cosas como automatizar el alumabrado para que parezca que estamos en casa, comprobar a distancia si las puertas y ventanas están cerradas, que dispositivos tengo activos, etc.

Pero también debemos hablar de eficiencia energética en cosas tan sencillas como que las luces se enciendan cuando nos acercamos y por supuesto de confort, es decir automatizar para hacernos la vida mas fácil.

La mejor forma de saber que automatizar es pensar y anotar aquellas cosas repetitivas que hacemos para automatizarlas. Para esto hay que abstraerse de todo aquello que hacemos de manera automática y sin pensarlo simplemente porque estamos muy acostumbrados a hacerlo.

Algunas ideas de cosas para automatirzar un piso o casa unifamiliar:

* Control remoto de persianas y ventanas.
* Control del calentamiento del agua en remoto.
* Control del consumo energético.
* Iluminación automatizada por presencia o por nivel de luz.
* Control de calefacción y ventilación eléctrica.
* Control automático de riego de plantas.
* Encendido y apagado de dispositivos en remoto.
* Control automático de puertas de garage.
* Notificaciones en el móvil de eventos que ocurren en los controles.

Cuando hablamos de domótica la forma mas sencilla y económica de implantarla es utilizando conexiones inalámbricas dada su flexibilidad y no requerir de técnicos especialistas. Si por el contrario hablamos de inmótica o urbótica el sistema cableado es sin duda el mejor, lo que no significa que se descarte totalmente el uso de dispositivos inalámbricos.

## <FONT COLOR=#007575>**1.2. Protocolos para domótica**</font>
Antes de nada debemos decidir que sistema o lenguaje de comunicación van a usar nuestros dispositivos. Según el protocolo que elijamos quedarán determinados los dispositivos y opciones futuras que deberán ser compatibles. Veamos brevemente cuales son los protocolos.

* **X10**. No necesita cableado porque utiliza los propios cables eléctricos para establecer las comunicaciones. Totalmente en desuso.
* **UPB**. Líneas eléctricas como bus universal (Universal Powerline Bus). Es un protocolo que vino a corregir las deficiencias del X10.
* **INSTEON**. Utiliza una tecnología mixta de comunicación a través de líneas eléctricas e inalámbrica. En desuso.
* **Z-Wave**. Tecnología estándar para la domótica inalámbrica. Es una red en malla que utiliza ondas de radio de baja energía para que los dispositivos se comuniquen. Los dispositivos funcionan también como repetidores permitiendo hasta 230 dispositivos en un solo controlador. Es compatible para todos los fabricantes que forman parte de su alianza. En este [enlace a eedomus documentación](https://doc.eedomus.com/es/index.php/Lista_de_dispositivos_Z-Wave) podemos consultar la lista de dispositivos Z-Wave probados.
* **ZigBee**. Muy similar a Z-Wave con mayor consumo y radiación que esta. No se recomienda utilizar dispositivos de distintos fabricantes.
* **Wi-Fi**. Uitiliza la red WiFi para el control de dispositivos. Su principal ventaja es lo fácil que es de utilizar y su principal problema es que requiere un gran ancho de banda para que los dispositivos inteligentes no tengan latencia por la interferencia de ordenadores, tablets, móviles, etc. Hay que tener en cuenta que el WiFi consume bastante energía por lo que las baterías o pilas de los dispositivos son un factor a tener en consideración.
* **Bluetooth**. Es la forma sencilla y segura de comunicarnos con dispositivos cuando las distancias son cortas (puertas o luces). Se suelen encontrar en sistemas híbridos con ZWave o Zigbee.

Como controladores por voz debemos buscar la compatibilidad con Google Home, Alexa o Apple para después comprobar que dispositivos son compatibles con él.
