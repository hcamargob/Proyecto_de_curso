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

### 2. Descrip

