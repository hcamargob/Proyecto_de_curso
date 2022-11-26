# Robótica - Proyecto Final

<p align="center">
ROBÓTICA

<p align="center">
Hugo Alejandro Camargo Barrera
<p align="center">
email: hcamargob@unal.edu.co

<p align="center">
Santiago Hernández Lamprea
<p align="center">
email: shernandezl@unal.edu.co


<p align="center">
INGENIERÍA MECATRÓNICA
<p align="center">
Facultad de Ingeniería
<p align="center">
Universidad Nacional de Colombia Sede Bogotá

Para cumplir satisfactoriamente los requerimientos y tareas propuestas, se siguió el siguiente proceso:
 ### 1. Descripción de la solución:
 El primer paso fue el diseño del griper, para esto, se tomó como referencia los vídeos publicados en la guía del proyecto. Todo este proceso fue realizado en el software _Autodesk Inventor_. El modelado del ensamble general fue el siguiente:
 
 ![image](https://user-images.githubusercontent.com/112737454/204070335-fbad7be3-7abd-4839-9118-7fe4b21c707c.png)

Teniendo estos ensambles completos, se exportaron estos modelos a RobotStudio, de tal manera que se pudiera tener concepción de los distintos TCP que tenía cada pieza. Al importarlos y obtener sus pocisiones, este fue el resultado:

![image](https://user-images.githubusercontent.com/112737454/204070503-7f19a9b3-eab2-402b-9af3-8015051bc281.png)

La siguiente consideración fue el porta herramientas, el cual debía permitir la succión y descanso de las ventosas. Así como con el griper, la herramienta se diseño en _Autodesk Inventor_ y se exporto a RobotStudio. El funcionamiento de las ventosas se controla a través de salidas digitales del controlo del robot, simplemente se integran a las trayectorias generadas por el software de ABB. El comportamiento de estas salidas a lo largo del código se muestran en el simulador de entradas y salidas.

![image](https://user-images.githubusercontent.com/112737454/204070770-1c80ecfa-70dd-41c6-a32f-a799b05dce1f.png).

Así pues, se determinaron zonas críticas, donde se activan las salidas digitales para la succión y posterior descenso de las piezas.

### 2. Descripción del Griper.
 
 Para el desarrollo del griper, se desarrolló una herramienta de 9 piezas, cumpliendo con el primer requerimiento de numero de piezas. las bases del griper son dos marcos cuadrados de 165 mm de lado. El émbolo usado es un perfil en T, con el mismo funcionamiento del mostrado en la guía. La te esta conectada a dos brazos que cierran el mecanismo con una semijunta que permite la apertura y cierre de las pinzas. Los planos de cada piezas son adjuntos a este repositorio. Esta es la distribución general de las piezas.
 
 ![image](https://user-images.githubusercontent.com/112737454/204071182-07907569-7771-4ade-b835-05560c226dfb.png)
 
 Se decidió realizar la manufactura de las piezas en MDF a través del proceso de corte laser. Así pues, se obtuvo el siguiente resultado:
 
 ![image](https://user-images.githubusercontent.com/112737454/204071355-85bf3f42-c82f-4301-a0ea-524c5ff6018b.png)

 Para facilidad del ensamble, se decidió acoplar las piezas de los brazos en uno solo, esto, buscando estabilidad de las piezas y evitando problemas dimensionales que afectaran la succión de las piezas.

 De esta manera se diseño la cama, donde caeran las piezas para el ensamble, y el resultado fue el siguiente:
 
![image](https://user-images.githubusercontent.com/112737454/204071574-714da8dc-0e64-45f8-8ef9-4b237336da34.png)
 
 ![image](https://user-images.githubusercontent.com/112737454/204071589-b09bd608-1d2b-4439-bb33-da0015f1f551.png)
 
 ### 3. Descripción de la herramienta
 
 Se diseñó una herramienta sencilla para la ventosa, limitandose a la base que encaja con el plato porta herramientas, y una L, que es el acople con la ventosa. 
 
 ![image](https://user-images.githubusercontent.com/112737454/204071841-1731c866-f51a-4de1-a71f-a21e00dda0b8.png)
 
 El soporte se realizó tenuendo en cuenta el largo del acople de la ventosa con el actuador neumático del laboratorio, teniendo una longitud de 60 mm. Esta herramienta se desarrolló a través de manufactura aditiva, está hecha en ácido poli-láctico (PLA), por eso se desarrollo en dos partes.
 
 ![image](https://user-images.githubusercontent.com/112737454/204072108-e13c329c-09e2-4eb0-83c6-9b887154ff61.png)

 ![image](https://user-images.githubusercontent.com/112737454/204072116-13fd1e00-d741-4c11-bc9f-81f198fc0d48.png)

 Los planos de la herramienta también se encuentran en el repositorio.
 
 ### 4. Ensamble en Robot Studio
 
 El primer paso fue la creación de la herramienta, la cual fue importada desde Inventor y se le asigna su respectivo TCP. 
 
 ![image](https://user-images.githubusercontent.com/112737454/204072394-c7d29f5f-d4f1-4652-9ba7-a08fc38d6db8.png)
 
 Ya teniendo la herramienta, se procedió a incluir las piezas de trabajo al entorno, de tal manera que existen dos elementos, la salida con la distribución inicial, y la llegada con el acoplamiento del griper. 
 
 ![image](https://user-images.githubusercontent.com/112737454/204072510-707d1647-aaa0-4ee2-bdad-5fb8b9f181e5.png)
 
 Finalmente, con esos puntos creados, se generan las trayectorias que debe seguir el _IRB\_140_ para cumplir con la misión. Las trayectorias creadas describen el tramo de una herramienta, hay una trayectoria para la sujeción y otra para la liberación de cada pieza. En la siguiente imagen se observa la trayectoria de sujeción del émbolo.
 
 ![image](https://user-images.githubusercontent.com/112737454/204072803-fd44e44a-4f63-4510-a5a0-7eea6f475f29.png)
 
 Ya con las trayectorias creadas, se procede a programar el RAPID. 
 
 ### 5. RAPID
 
 

 
 
 
 El paso siguiente fue ubicar los distintos TCP para poder generar las trayectorias que debe seguir el robot. Para esto, se tomaron 3 puntos de movimiento por pieza: el punto donde la herramienmta entra en contacto con la pieza, el punto cercano a la pieza, donde empieza la succión y la velocidad disminuye y un punto que evita movimientos bruscos. En la siguiente imagen se muestra como se crearon esos TCP
 
 ![image](https://user-images.githubusercontent.com/112737454/204072648-e2719e11-44d1-4e74-8316-7de8da91149d.png)
 
 

 
 


 




