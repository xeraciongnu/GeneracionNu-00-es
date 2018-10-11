---
description: Laboratorio Android - Es Android software libre?
---

# Repositorios de Software Libre en Android​

![](.gitbook/assets/image%20%2849%29.png)

## Repositorios de Software Libre en Android​

### Es Android software libre?

Android es un sistema operativo, desarrollado en la actualidad por Google, que se encuentra instalado en millones de dispositivos como smartphones, tablets, smartwatches, televisores, … Aunque está basado en el Kernel de Linux, Android tiene componentes propietarios por lo que no es software libre \(o, por lo menos no en su totalidad\).

![](.gitbook/assets/image%20%281%29.png)

Para definir el escenario en el que nos encontramos y sobre el que hablaremos, supongamos que tenemos un dispositivo con una versión de Android instalada y funcionando \(este es el caso típico cuando adquirimos un dispositivo Android\). Ese dispositivo está preparado para funcionar pero puede que no tenga todos los programas que necesitamos y tendremos que recurrir a instalarlos posteriormente. Las aplicaciones que se pueden utilizar en Android están basadas en un sistema de gestión de paquetes que nos permite automatizar el proceso de instalación, configuracion y actualización de las mismas. El nombre \(sistema de gestión de paquetes\) es debido a que los programas se distribuyen en forma de “paquetes” \(con formato APK en el caso de Android\), encapsulados en un sólo fichero que contiene los ficheros necesarios para el correcto funcionamiento del programa en cuestión y, además, incluye información adicional como puede ser la versión, descripción, dependencias, …

Para instalar software en Android simplemente tendremos que descargar el fichero APK, ejecutarlo y seguir las instrucciones del proceso de instalación. Como esta práctica se antoja arriesgada \(cualquiera puede hacernos llegar un APK -no testado- que puede producir efectos no deseados en nuestro sistema\) Google ha implementado una “tienda” de software desde la cual podemos descargarnos los programas que necesitemos \(unos gratuitos y otros de pago\) de una manera sencilla y desde un entorno \(presumiblemente\) controlado y seguro. Esta “tienda” se llama Google Play Store \([https://play.google.com/store](https://play.google.com/store)\). Google Play Store es algo más que un repositorio de software. Es una plataforma de distribución digital de software \(para dispositivos Android\) y una tienda online que nos ofrece otro tipo de “productos” como peliculas, música, libros, ….

![Fuente de la imagen:  https://play.google.com/store ](.gitbook/assets/image%20%2875%29.png)

###  Es Google Play un repositorio de software libre?

Google Play Store es, efectivamente, un repositorio de software \(entre otras cosas, como hemos comentado\) pero, en su mayor parte, el software que contiene es propietario, incluso del software libre que ofrece no permite descargar los fuentes. Por lo tanto, la respuesta es NO; Google Play NO es un repositorio de software libre. Además, existen otras limitaciones impuestas por Google que pueden no ser de nuestro agrado \(como por ejemplo, la de exigir una cuenta de gmail para poder acceder a la Play Store\).

### Cuál es la alternativa, pues?

Si nuestra pretensión es disponer de un repositorio de programas para Android, que sean software libre o de fuentes abiertas y que no nos obligue a “darnos de alta” o a disponer de una cuenta de correo electronico asociada, nuestra elección debiera ser F-DROID \([https://f-droid.org/es/](https://f-droid.org/es/)\)

![Fuente de las im&#xE1;genes:  https://f-droid.org/&#xE9;/](.gitbook/assets/image%20%2874%29.png)

### Cómo obtener e instalar F-Droid?

 F-Droid no se puede descargar desde la Play Store de Google, por lo que deberemos ir a su web, descargar el APK e instalarlo manualmente en nuestro sistema. La ruta de descarga de la última versión es [https://f-droid.org/FDroid.apk](https://f-droid.org/FDroid.apk)

 Si lo preferimos, podemos hacer uso de un código QR para proceder a la descarga:

![Fuente de la imagen: https://f-droid.org/&#xE9;/](.gitbook/assets/image%20%2848%29.png)

 Una vez descargado el fichero APK procederemos a su instalación, localizándolo en la carpeta de “Descargas” correspondiente y ejecutándolo \(pulsando sobre él\). Para que este procedimiento funcione, previamente deberemos indicarle a nuestro dispositivo que le permitimos instalar programas “externos” a la Play Store de Google puesto que, como ya hemos comentado, Android por defecto sólo deja instalar software de su propia “tienda”. Para ello iremos a AJUSTES, generalmente en el apartado de “Seguridad”, buscaremos la opción “Fuentes Desconocidas” \(permitir la instalación de aplicaciones de orígenes distintos a la Play Store\) y la habilitaremos.

 Una vez instalado F-Droid tendremos acceso a un completo repositorio FOSS \(Free and Open Source Software\) que contiene todo tipo de aplicaciones y juegos. Además, dispondremos de acceso a un Foro de ayuda, a la documentación del proyecto, tutoriales, ... incluso nos explican cómo montar nuestro propio repositorio de software \(con repomaker\).

 Pero esa ya es otra historia...



### [Siguiente artículo](edicion-profesional-de-audio-con-linux.md)

