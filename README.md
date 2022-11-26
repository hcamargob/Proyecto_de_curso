# Proyecto_de_curso
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
 
 Para el desarrollo del griper, se desarrolló una herramienta de 9 piezas, cumpliendo con el primer requerimiento de numero de piezas. las bases del griper son dos marcos cuadrados de 165 mm de lado. El émbolo usado es un perfil en T, con el mismo funcionamiento del mostrado en la guía. La te esta conectada a dos brazos que cierran el mecanismo con una semijunta que permite la apertura y cierre de las pinzas. Los planos de cada piexas son adjuntos a este repositorio. Esta es la distribución general de las piezas.
 
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
 
 




