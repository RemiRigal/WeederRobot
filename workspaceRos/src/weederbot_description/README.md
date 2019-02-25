# Weederbot Description

Package ROS contenant la description physique du robot Weederbot.


## Affichage

Pour faciliter la modélisation et le debuggage il est possible de visualiser le robot sous Rviz.
```
roslaunch weederbot_description display.launch
```
Une instance du `Joint State Publisher` en interface graphique démarre afin de faciliter la visualisation des mouvements des joints.


## Utilisation dans d'autres packages

Pour charger la description du robot dans un autre fichier `launch` il suffit d'inclure le fichier `description.launch`.
```xml
<include file="$(find weederbot_description)/launch/description.launch"/>
```
Ce fichier démarre également une instance du `Robot State Publisher` qui publie automatiquement la TF du robot.
