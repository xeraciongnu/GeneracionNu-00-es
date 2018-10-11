---
description: 'Introducción: Latencia, Kernel RT (lowlatency) y Jack'
---

# ​Edición profesional de audio con Linux​

![](.gitbook/assets/image%20%2817%29.png)

## ​Edición profesional de audio con Linux​

### Introducción: Latencia

La pregunta que debemos hacernos es sí podemos abordar de una manera profesional la creación, edición y/o producción de audio desde Linux haciendo uso, exclusivamente, de software libre.

![CC0 Creative Commons - https://pixabay.com/es/sonido-ola-forma-de-onda-aural-1781569/](.gitbook/assets/image%20%2882%29.png)

Para poder responder adecuadamente a esta cuestión, debemos empezar por considerar el \(espinoso\) tema de la **latencia**. Sin meternos en temas demasiado sesudos, podemos definir latencia de audio como el tiempo que transcurre entre el momento de la emisión de un sonido y el momento en el que se escucha. Es decir, es un retardo que se aprecia entre la generación de un sonido y el sonido propiamente dicho.

Es un tema fundamental puesto que, aunque no es posible conseguir la latencia cero -lo explicaremos más adelante-, es necesario que la latencia existente no sea apreciable para el oído humano o nos resultaría imposible manejar el sistema, “tocar” o “interpretar” los sonidos en tiempo real.

Veamos, el sonido se propaga a una velocidad de 340 metros por segundo; es decir, si emitimos un sonido a una distancia de un metro, tardaremos en escucharlo algo menos de 3 milisegundos \(concretamente 2’9 milisegundos\). Bajo esta premisa, nos percatamos de que cualquier músico asume cierta latencia implícita.

![CC0 Creative Commons - https://pixabay.com/es/guitarra-guitarra-cl%C3%A1sica-756326/](.gitbook/assets/image%20%2877%29.png)

Por ejemplo, un guitarrista \(acústico\) tiene la fuente de sonido a unos 40 cm por lo que tardará cerca de 1 milisegundo en escucharlo. Un violinista \(está a unos 10 cm de su fuente de sonido\) unos 0’3 milisegundos. Un guitarrista eléctrico, si se encuentra a unos 3 metros del amplificador, tendrá que soportar una latencia de 9 milisegundos.  
Este ejemplo se puede complejizar todavía más si pensamos en un grupo de varios instrumentistas tocando en distintas partes de un escenario e intentando tocar todos juntos y acompasados. Pero ese no es el tema que nos ocupa por lo que lo dejaremos para mejor ocasión.

Un ordenador, como ya hemos dicho, también tiene latencia pero, en este caso, no se debe a la distancia entre el emisor y el receptor si no entre la generación del sonido y la emisión efectiva del mismo. Igualmente, que en el caso anterior, hay ciertos límites de latencia admisibles \(por ser imperceptibles por el oído humano\).  
**Por lo general podemos admitir, para un sistema “en tiempo real”, una latencia de 11 milisegundos.**

###  Kernel RT \(lowlatency\)

Cómo abordamos, pues, el tema de la latencia de audio de un ordenador que funcione bajo el Sistema Operativo GNU/Linux? La respuesta es sencilla: utilizando un Kernel RT \(lowlatency o de baja latencia\). El Kernel “normal” de Linux es multitarea y tiene un sistema de control de prioridades pero no podemos interrumpir los procesos en “cualquier sitio” y ahí es donde aparece la latencia. Un Kernel RT controla la prioridad de los procesos y es capaz de gestionar de una manera más eficiente esa latencia.

![CC0 Creative Commons - https://pixabay.com/es/plato-giratorio-vista-superior-1337986/](.gitbook/assets/image%20%2832%29.png)

También podemos contribuir a disminuirla utilizando hardware más moderno y potente. De hecho, para un uso no intensivo del procesamiento de señal de audio no es necesario disponer de un kernel de baja latencia, simplemente llegará con un hardware adecuado.  
Un ejemplo sería el procesado de audio con Audacity: podemos grabar o editar audio sin necesidad de tener instalado un kernel de baja latencia.

Si quisiéramos instalar un Kernel RT en GNU/Linux \(por ejemplo en una distro de la rama Debian\) debiéramos hacerlo de la siguiente manera:

```text
sudo apt-get install linux-headers-lowlatency
sudo apt-get install linux-lowlatency
sudo update-grub
```

###  Jack

Una vez instalado el Kernet RT, para poder gestionar las conexiones de audio entrantes y salientes en nuestro sistema operativo Linux, usaremos JACK \(Jack Audio Conection Kit, [http://jackaudio.org/](http://jackaudio.org/)\) que es un servidor de sonido que provee conexiones de baja latencia entre aplicaciones.

Esta es la pantalla principal de QjackCt \([https://qjackctl.sourceforge.io/](https://qjackctl.sourceforge.io/) una interfaz gráfica de jack que nos ayuda a la hora de interactuar con el programa\)

![Fuente de las im&#xE1;genes: https://qjackctl.sourceforge.io/qjackctl-screenshots.html](.gitbook/assets/image%20%289%29.png)

Y esta es la ventana de configuración donde podemos observar \(abajo a la derecha\) que con esa configuración se consigue una latencia de 5’8 milisegundos \(cualquier valor por debajo de 11 milisegundos es más que aceptable\).

![](.gitbook/assets/image%20%2827%29.png)

Una vez configurado JACK \(cosa de la que nos ocuparemos en otro momento\) estamos en disposición de empezar a trabajar con nuestro software de audio \(composición, edición, producción, …\) en nuestra distribución de GNU/Linux favorita. De hecho, existen distribuciones específicas de Linux para el tratamiento de audio a todos los niveles \(Ubuntu Studio, KXStudio, Musix, AVLinux, ...\).  
Tanto la configuración del servidor de audio JACK, como la elección del software que queremos usar y/o la distribución más adecuada son temas que trataremos más adelante.

**Hasta luego y que no pare la música!**



### [Siguiente artículo](dibujos-libres.md)

