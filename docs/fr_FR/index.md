# Plugin Powerlink 2

![GitHub Logo](/../images/pmax.jpg)


Le plugin Powerlink permet de communiquer avec les alarmes Visonic par l’intermédiaire du module Powerlink 2.
Il permet de connaitre le statut de la centrale et des détecteurs. (Prêt, Non Prêt, Ouvert, En Alarme, etc…)
Le plugin a été mis à jour pour fonctionner sur Jeedom v4.

>Le détecteur de mouvement ne génère pas de statut dans le module Powerlink (sauf en alarme) Il n’est donc pas possible de connaitre son statut. 

## Installation :
Il n’y a pas d’installation particulière à prévoir. Le plugin se connecte avec le module Visonic Powerlink par IP comme un navigateur internet.
Un démon local est démarré par le plugin et communique par défaut toutes les 5 secondes avec Powerlink.

## Configuration Général
Après le téléchargement du plugin, il vous suffit de l’activer et de le configurer.
Commencer par créer l'équipement de type "Centrale".
Indiquer l’adresse IP du module Powerlink. L’adresse par défaut est généralement 192.168.1.200
Indiquer le port, par défaut le port HTTP est 80.
Indiquer le nom d’utilisateur, par défaut Admin.
Indiquer le mot de passe, par défaut Admin123.

>Il faut respecter la casse pour le mot de passe et le nom d’utilisateur. 

## Configuration des détecteurs
Chaque détecteur est représenté comme un équipement.
Dans le type il faut donc indiquer la zone correspondant à la centrale précédemment créé.
Inutile de renseigner ici l'IP, port, utilisateur et mot de passe.

## Configuration des commandes
Il est possible d’ajouter soit des infos, soit des actions.

Chaque commande de type info ajouté correspond à la zone de l'équipement créé.
Chaque action ajoutée correspond l'équipement centrale même si elle ajouter sur une zone.

L'information peut être de type texte (Pret, Total, etc...) et de type binaire (0 ou 1).
Les informations de type binaire permettent d'historiser et de créer des scénarios beaucoup plus simplement.

## Batteries
L'alarme retourne uniquement l'état des piles au moment du changement.
Par défaut le niveau dans Jeedom est 100% et passera à 5% en cas de besoin.

