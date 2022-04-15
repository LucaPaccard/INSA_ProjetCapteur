# Codes Arduino

Deux codes ont été développés pour proffiter au mieux des fonctionnalités de notre capteur.

## Sommaire

* [Graphite_sensor](#PremiereSection)
* [Angle_calibration](#DeuxiemeSection)


## Graphite_sensor <a id="PremiereSection"></a>
Ce [premier code Arduino](https://github.com/MOSH-Insa-Toulouse/2021-2022_Paccard_Lemaire_Projet_Capteur/blob/main/Arduino/Angle_calibration/Angle_calibration.ino) permet d'afficher un menu contenant quatre sous-menus.
* Le premier sous-menu permet d'afficher en direct la valeur de résistance du capteur et la tension lue par la carte Arduino.
* Le deuxième sous-menu permet de choisir un calibre pour l'affichage de la résistance dans le premier menu. Les calibres disponibles sont : Ω, kΩ et MΩ.
* Le troisème sous-menu permet d'afficher la durée d'execution du programme.
* Le dernier sous-menu permet d'afficher une image.

## Angle_calibration <a id="DeuxiemeSection"></a>
Ce [second code Arduino](https://github.com/MOSH-Insa-Toulouse/2021-2022_Paccard_Lemaire_Projet_Capteur/blob/main/Arduino/Graphite_sensor/Graphite_sensor.ino) permet d'effectuer un calcul d'angle par rapport à la calibration du capteur. 
L'utilisateur rentre les valeurs de la résistance à plat et à la position la plus courbée possible. En considérant la variation de résistance linéaire, un produit en croix est ensuite fait pour asssocier une valeur de résistance à un angle de déformation.
