![logo](https://github.com/paxo-phone/paxo-electronic/assets/45568523/3084b431-1ca6-4c1e-95bb-b80da2699dba)

Ce répertoire rassemble tous les fichiers relatifs au hardware du projet Paxo (plans, modèles 3D etc.) permettant à chacun d'étudier le fonctionnement du téléphone et / ou de le fabriquer chez soi. 

# Schéma
Disponible en PDF ici: [https://github.com/paxo-phone/paxo-electronic/blob/main/schematic.pdf](https://github.com/paxo-phone/paxo-electronic/blob/main/schematic.pdf)
Et sur ovhlab ici: [https://oshwlab.com/gabriel.rochet/paxo-phone-5-r1](https://oshwlab.com/gabriel.rochet/paxo-phone-5-r1)

# Architecture générale

Le circuit est basé sur 6 parties essentielles.

- **L’ESP32** est le microcontrôleur, le “cerveau” du téléphone : avec 2 cœurs à 240Mhz, il se charge de réaliser tous les calculs et de faire tourner l’OS. Il s’occupe de faire les rendus de l’écran et de synchroniser tous les autres composants.
- **Le SIMCOM A7682E** est un composant permettant la connexion et la communication au réseau **4G**. Il se charge de passer les appels, en utilisant le microphone et le haut-parleur. Il permet également de connaître l’heure exacte en fonction de la localisation, analyse la charge de la batterie, et permet l'accès a internet via la 4G.
- **Le CH340C** est un convertisseur USB vers TTL. Il permet à l’ESP32 de communiquer avec un ordinateur par le port USB. Il permet donc de mettre à jour le téléphone et de mieux comprendre les calculs en temps réel de l’esp32.
- Le circuit d’alimentation utilise 3 composants distincts : le premier sert à charger la batterie depuis le port USB, le second est utilisé pour sécuriser la charge et la décharge de la batterie et lui garantir une longue vie, et le dernier permet de convertir l’énergie de la batterie en un voltage utilisable par tout le reste du circuit.
- La mémoire SPI est assurée par une carte micro SD. L’ESP32 a un stockage très limité et doit donc utiliser une mémoire externe pour stoker les messages, les images et etc.
- **L’écran 320x480**, avec un tactile capacitif, il permet l’affichage de l’interface utilisateur et l’exploitation de l’OS.

# Nous contacter

Vous pouvez nous contacter via notre [site web](https://www.paxo.fr) ou notre [serveur discord](https://discord.com/invite/MpqbWr3pUG).

# En savoir plus

Visiter [notre site](https://www.paxo.fr) pour en savoir plus sur le projet Paxo.

# Contributeurs 

<a href="https://github.com/paxo-phone/PaxOS-8/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=paxo-phone/paxo-electronic" />
</a>
