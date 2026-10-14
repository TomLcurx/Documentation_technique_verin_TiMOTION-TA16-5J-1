# Vérin électrique TiMOTION TA16-5J-1

### *Documentation réalisée par essais, répertoriés dans Rapport_de_tests.md*

## 1. Présentation générale

Le **TiMOTION TA16-5J-1** est un actionneur linéaire électrique permettant de convertir l'énergie électrique en un mouvement mécanique de translation. Il est utilisé pour réaliser des mouvements de poussée et de traction afin de déplacer, lever ou positionner un élément mécanique.

<img src="images/verin.jpg" alt="Vérin TiMOTION TA16-5J-1" width="400">
*Figure 1 — Vue générale du vérin électrique TiMOTION TA16-5J-1.*
<br>

</br>
Cet actionneur peut être intégré dans différents systèmes automatisés nécessitant un déplacement linéaire motorisé. Son intégration dépend notamment des contraintes mécaniques, électriques et environnementales de l'application.

## 2. Principe de fonctionnement

Le vérin fonctionne grâce à un moteur électrique qui entraîne un mécanisme de transmission interne. Ce mécanisme transforme la rotation du moteur en un déplacement linéaire de la tige.

Selon le sens de commande du moteur, la tige sort ou rentre, permettant ainsi de modifier la position de l'élément mécanique auquel elle est reliée.

Le pilotage du vérin nécessite une alimentation électrique et un système de commande adaptés à ses caractéristiques nominales.

## 3. Caractéristiques techniques

Les caractéristiques relevées sur l'actionneur TiMOTION TA16-5J-1 sont les suivantes :

| Paramètre | Valeur |
|---|---|
| Fabricant | TiMOTION |
| Référence | TA16-5J-1 |
| Tension d'alimentation | 24 V DC |
| Facteur de marche (*Duty cycle*) | 10 % |
| Durée maximale de fonctionnement continu | 2 minutes |
| Temps de repos indiqué | 18 minutes |
| Charge indiquée (*Load*) | 2 000 N |
| Courant maximal (*Current*) | 4,25 A |
| Sortie minimale de la tige, vérin replié | 24 mm |
| Sortie maximale de la tige | 164 mm |
| Course utile de la tige | 140 mm |

### 3.1. Tension d'alimentation

Le vérin fonctionne sous une tension d'alimentation de **24 V en courant continu (DC)**. L'alimentation et le système de commande doivent être compatibles avec cette tension.

### 3.2. Course de la tige

La tige présente une sortie minimale de **24 mm** lorsque le vérin est en position repliée, et une sortie maximale de **164 mm** lorsqu'elle est complètement déployée.

La course utile correspond à la différence entre ces deux positions :

Course utile = 164 mm - 24 mm = 140 mm

Le déplacement linéaire exploitable de la tige est donc de **140 mm**.


<img src="images/verin_min.jpg" alt="Vérin TiMOTION rétracté TA16-5J-1" width="400">
*Figure 2 — Vérin rétracté au maximum.*
<br>

</br>


<img src="images/verin_max.jpg" alt="Vérin TiMOTION déplié TA16-5J-1" width="400">
*Figure 3 — Vérin déplié au maximum.*
<br>

</br>

### 3.3. Facteur de marche

Le facteur de marche est de **10 %**, avec un cycle de fonctionnement indiqué de 2 minutes en marche et 18 minutes à l'arrêt. Cette limitation doit être respectée afin de prévenir une surchauffe et une usure prématurée de l'actionneur.

### 3.4. Charge

La charge indiquée est de **2 000 N**. Cette valeur correspond à un effort équivalent au poids d'une masse d'environ 204 kg dans les conditions de la gravité terrestre. Cette équivalence ne constitue pas une garantie de capacité de levage : l'effort admissible dépend des conditions de montage et d'utilisation.

### 3.5. Courant électrique

Le courant maximal indiqué est de **4,25 A**. L'alimentation électrique et le dispositif de commande doivent être dimensionnés en tenant compte de cette valeur et des éventuels appels de courant au démarrage (la documentation officielle prévoit jusqu'au double de la valeur initiale lors du démarrage du moteur).

## 4. Connexions électriques et brochage

Cette section décrit les connexions électriques du vérin TiMOTION TA16-5J-1 afin de faciliter son raccordement à un système de commande.

### 4.1. Connecteur

Le vérin est équipé d'un connecteur électrique permettant de relier l'actionneur à son alimentation et à son système de commande.

Ce dernier est un connecteur Molex Mini Fit Jr de 8 pins.

<img src="images/connecteur.jpg" alt="Vérin TiMOTION TA16-5J-1" width="400">
*Figure 4 — Connecteur du vérin TiMOTION TA16-5J-1.*

### 4.2. Identification des fils

Les conducteurs électriques doivent être identifiés avant le raccordement. Pour chaque fil, il convient de préciser sa couleur, sa fonction et sa connexion au système de commande.

<img src="images/cables.jpg" alt="Vérin TiMOTION TA16-5J-1" width="400">
*Figure 5 — Fils de commande du vérin TiMOTION TA16-5J-1.*
<br>

</br>

| Couleur du fil | Fonction électrique |
|---|---|
| JAUNE | VDC +24V (extension) / ±0V (rétractation) |
| VERT | VDC +24V (rétractation) / ±0V (extension) |
| ROUGE | VCC +5V |
| NOIR | GND |
| BLANC | Signal hall 1 |
| BLEU | Signal hall 2 |

## 4.3. Fonctionnement des capteurs à effet Hall

Les capteurs Hall permettent de détecter les variations d'un champ magnétique et de produire des signaux électriques. Dans un vérin équipé de ces capteurs, les signaux permettent de suivre le mouvement du mécanisme.

Les deux signaux, S1 et S2, peuvent notamment être utilisés pour :

- compter les impulsions générées pendant le déplacement ;
- estimer le déplacement de la tige après calibration ;
- suivre le mouvement du vérin ;
- déterminer le sens de déplacement si le déphasage entre les deux signaux le permet.

Les capteurs Hall ne fournissent pas nécessairement une position absolue au démarrage. Une référence initiale peut donc être nécessaire pour connaître la position de la tige.

La fiche technique officielle de la série TA16 indique des capteurs Hall de type NPN avec une plage de tension spécifiée de +5V à +36V et pour le TA16-5J-1, la tension prévue est de +5V.

### 5. Objectif de cette documentation

Cette documentation technique a été réalisée afin de centraliser les informations relatives au vérin électrique TiMOTION TA16-5J-1 et de faciliter son utilisation dans le cadre du projet.

Auparavant, cet actionneur n'avait pas encore été utilisé dans le cadre du projet. Les informations concernant ses caractéristiques techniques, son fonctionnement et ses connexions électriques n'étaient donc pas toutes connues ou documentées.

L'objectif de ce travail est ainsi d'identifier les caractéristiques du vérin, de clarifier son principe de fonctionnement et de déterminer les modalités de raccordement nécessaires à son intégration dans le système.

Cette documentation constitue une base de référence pour les futures utilisations du vérin. Elle permet de conserver les informations collectées et de faciliter les opérations de montage, de raccordement, de mise en service et de maintenance.


### 6. Documentation constructeur

Pour obtenir des informations complémentaires sur les dimensions, la course, la vitesse de déplacement et les possibilités de retour de position, il convient de consulter la documentation technique correspondant à la référence exacte du vérin.

[Consulter le documentation officielle de TiMOTION](([https://www.timotion.com/_upload/files/DataSheet_TA16-V_EN.pdf](https://www.timotion.com/_upload/files/DataSheet_TA16-V_EN.pdf)))

*Remarque : les caractéristiques présentées ci-dessus reprennent les indications relevées sur l'actionneur. Les paramètres non indiqués, notamment la course, la vitesse et le type de retour de position, restent à confirmer à partir de la documentation constructeur.*\
