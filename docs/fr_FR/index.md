# Plugin Powerlink

![GitHub Logo](/../images/pmax.jpg)


Le plugin Powerlink permet de communiquer avec les alarmes Visonic par l’intermédiaire du module Powerlink 2.
Il permet de connaitre le statut de la centrale et des détecteurs. (Prêt, Non Prêt, Ouvert, En Alarme, etc…​)

>Le détecteur de mouvement ne génère pas de statut dans le module Powerlink (sauf alarme) Il n’est pas possible de connaitre son statut. 

## Installation :
Il n’y a pas d’installation particuliere à prévoir. Le plugin se connecte avec le module Visonic Powerlink par IP.
Un démon local est démarré par le plugin et communique toutes les 5 secondes avec Powerlink. Le démon vérifie toutes les 15 minutes que le plugin fonctionne correctement, sinon il le relance.


## Configuration Général
Après le téléchargement du plugin, il vous suffit de l’activer et de le configurer.
Indiquer l’adresse IP du module Powerlink. L’adresse par défaut est généralement 192.168.1.200
Indiquer le port, par défaut le port HTTP est 80.
Indiquer le nom d’utilisateur, par défaut Admin.
Indiquer le mot de passe, par défaut Admin123.

>Il faut respecter la casse pour le mot de passe et le nom d’utilisateur. 

## Configuration des commandes
Il est possible d’ajouter soit des statuts de zone, soit des commandes.
Pour chaque statut ajouter, il faut indiquer : Le nom Le type (statut) ** La zone (correspond à la zone paramétré dans l’alarme)

>Les statuts sont indiqués par des valeurs numériques. Il est donc possible de les historiser. 
>Pour chaque commande ajouter, il faut indiquer : Le nom Le type (commande) ** La commande (Armement Total, Armement Partiel ou Désarmer)
