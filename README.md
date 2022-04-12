# 2021-2022_Paccard_Lemaire_Projet_Capteur
Ce projet s'inscrit dans l'UF **"Du capteur au banc de test"** en 4ème année au département de Génie Physique de l'INSA Toulouse.
***
L'objectif de ce dernier est d'élaborer un **capteur de déformation** low-tech à base de graphite. L'application d'une contrainte mécanique sur un capteur en papier sur lequel un dépôt de crayon à papier à été fait, modifie la distance entre les particules de graphite. La conductivité électrique de la couche de graphite est elle aussi modifiée et celà induit une variation de la résistance. C'est cette donnée qui va nous intéresser.
L'ensemble des étapes menées pour réaliser ce capteur, en allant du **design** jusqu'à la **réalisation** en passant par le **codage** seront détaillées dans ce dossier.

## Sommaire
* [1. Description du projet et détail des livrables](#PremiereSection)
* [2. Arduino](#DeuxiemeSection)
  * [2.1. Librairies utilisées](#DeuxiemeSection1)
  * [2.2. Code Arduino](#DeuxiemeSection2)
* [3. Application Android](#TroisiemeSection)
* [4. KICAD](#QuatriemeSection)
  * [4.1. Symboles et empreintes des composants](#QuatriemeSection1)
  * [4.2. Schématique](#QuatriemeSection2)
  * [4.3. Placement des composants](#QuatriemeSection3)
  * [4.4. Visualisation 3D](#QuatriemeSection4)
* [5. Fabrication du shield](#CinquiemeSection)
  * [5.1. Réalisation du PCB](#CinquiemeSection1)
  * [5.2. Perçage et soudure](#CinquiemeSection2)
* [6. Banc de test](#SixiemeSection)
  * [6.1. Banc de test](#SixiemeSection1)
  * [6.2. Résultats obtenus](#SixiemeSection2)
  * [6.3. Analyse des résultats et pistes d'améliorations](#SixiemeSection3)
* [7. Datasheet](SeptiemeSection)

## 1. Détail des livrables et description du projet <a id="PremiereSection"></a>
Voici l'ensemble des livrables du projet :
- Un **shield PCB** se connectant à une carte **Arduino UNO** contenant un amplificateur transimpédance, un module bluetooth, un écran OLED et un encodeur rotatoire
- Un **code Arduino** permettant de mesurer la déformation du capteur et de piloter le module bluetooth, l'écran OLED et l'encodeur rotatoire
- Une **application Android APK**
- Un **protocole de test** 
- La **datasheet** du capteur de déformation

Tout d'abord, nous avons réalisé un code Arduino permettant de vérifier notre montage contenant un amplificateur transimpédance, un écran OLED, un module bluetooth et un encodeur rotatoire. Une fois le montage fonctionnel, nous avons réalisé le design de notre shield sur le logiciel *KICAD*. Nous l'avons ensuite fabriqué et assemblé (lithographie, perçage, soudage des composants, etc.). En parallèle de cela, nous avons utilisé le logiciel *MIT App Inventor* afin de développer une application Android APK, capable de communiquer et recevoir les informations envoyées par le module bluetooth telles que les valeurs de résistance du capteur mesurées. Nous avons par la suite mis en place un banc de test pour pour caractériser les différents types de capteurs en fonction de leur déformation et de la mine de crayon utilisée (HB, B, 9B, etc.). Enfin, nous avons établi une datasheet à l'aide des résulats obtenus par le banc de test.

## 2. Arduino <a id="DeuxiemeSection"></a>
### 2.1. Librairies utilisées <a id="DeuxiemeSection1"></a>
Nous avons utilisé différentes librairies dans notre code Arduino. La librarie ["Adafruit_SSD1306"](/Libraries/Adafruit_SSD1306) permet de contrôller l'écran OLED. La librairie [""Adafruit_BusIO"](/Libraries/Adafruit_busIO) permet de gérer la connexion en I2C et SPI.

### 2.2. Code Arduino <a id="DeuxiemeSection2"></a>
Le code Arduino, développé sous Arduino IDE contient plusieurs fonctionnalités. Il permet d'assurer la communication entre la carte Arduino, qui récupère la valeur de tension renvoyée par le capteur, et les différents éléments ajoutés sur le shield soit : l'écran OLED, le module bluetooth et l'encodeur rotatoire. Différents menus sont accessibles sur l'écran OLED :
* Le premier menu permet un simple affichage de la résistance
* Le deuxième menu permet de selectionner le calibre de la résistance affichée sur le menu 1. Cette dernière peut ainsi être affichée en Ohm, kOhm ou MOhm.
* Le troisème menu est un chronomètre permettant de savoir le temps d'éxecution du programme. C'est à dire le temps depuis le programme à été démarré.
* Le quatrième menu permet l'affichage d'une image.

Les codes sont contenus dans les dossiers :

## 3. Application Android <a id="TroisiemeSection"></a>

## 4. KICAD <a id="QuatriemeSection"></a>
### 4.1. Symboles et empreintes des composants <a id="QuatriemeSection1"></a>
* Amplificateur LTC1050

<img src="/Images/LTC1050_schematic.png" height="200"> <img src="/Images/LTC1050_footprint.png" height="200">

* Ecran OLED

<img src="/Images/OLED_schematic.png" height="200"> <img src="/Images/OLED_footprint.png" height="200">

* Encodeur rotatoire KY_040

<img src="/Images/KY_040_schematic.png" height="200"> <img src="/Images/KY_040_footprint.png" height="200">

* Module bluetooth HC05

<img src="/Images/Bluetooth-HC05_schematic.png" height="200"> <img src="/Images/Bluetooth_HC05_footprint.png" height="200">


### 4.2. Schématique <a id="QuatriemeSection2"></a>
<img src="/Images/Schematique_globale.png">

Une fois les empreintes créées, nous avons réalisé le schéma de notre shield. En haut à droite sont représentées les broches de la carte Arduino. En haut au milieu est représenté l'amplificateur transimpédance et en bas du schématique se trouvent l'écran OLED, le module bluetooth et l'encodeur rotatoire.

### 4.3. Placement des composants <a id="QuatriemeSection3"></a>

### 4.4. Visualisation 3D <a id="QuatriemeSection4"></a>

## 5. Fabrication du shield <a id="CinquiemeSection"></a>
### 5.1. Réalisation du PCB <a id="CinquiemeSection1"></a> 

### 5.2. Perçage et soudure <a id="CinquiemeSection2"></a> 

## 6. Banc de test <a id="SixiemeSection"></a> 
### 6.1. Banc de test <a id="SixiemeSection1"></a> 

### 6.2. Résultats obtenus <a id="SixiemeSection2"></a> 

### 6.3. Analyse des résultats et pistes d'améliorations <a id="SixiemeSection3"></a> 

## 7. Datasheet <a id="SeptiemeSection"></a> 
