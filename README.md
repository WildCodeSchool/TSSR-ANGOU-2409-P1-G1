![KEYPASS](https://img.linuxfr.org/img/68747470733a2f2f6b6565706173732e696e666f2f696d616765732f69636f6e732f6b6565706173735f333232783133322e706e67/keepass_322x132.png)

Projet : 
# _**Gestion Base De Données Securisée De Mots De Passes**_

# Documentation Générale

## Introduction

La gestion des mots de passes dans une entreprise est toujours un sujet délicat et très technique.
D'une part la sécurité d'un système d'information est fortement lié a ces mots de passes, de l'autre les techniques pour compromettre ces "sésames" sont de plus en plus sophistiqués.
l'utilisation de mots de passes fort doit être le but de tous !
Cependant, cela signifie de créer comme mot de passe une phrase complexe souvent impossible à retenir de mémoire. 
Mais alors, comment gérer efficacement le stockage de ces mots de passes ?
Essayons d'y répondre...

## Présentation du projet 

Le but de ce projet est de gérer, administrer et maintenir une Base De Donnes Securisée De Mots De Passe en mode clients/serveur.
Cette base de données sera gérer avec le logiciel Keypass et sera accessible aux administrateurs et aux utilisateurs du SI de l'entreprise.
La base de données pour les administrateurs serà isolé de la base de données pour les utilisateurs (Repertoire partagé différent / droits différents / clef d'accès différente)


##  Mise en contexte

KeePass est un outil, sous licence GPL v2 ou ultérieure, qui permet non seulement la gestion raisonnée et organisée des mots de passe, mais offre également de très pratiques raccourcis et autres facilités qui soulagent le quotidien.
cet outil sera installé sur un serveur et accessible depuis n'importe quel poste et n'importe quel client connecté au réseau de l'entreprise.
Une maquette sera réalisé avec un serveur et un poste client dans un environnement Windows sur un réseau local (IP fixes)
La méthode Agile sera utilisé pendant cette phase.

## Rôles de chaque membre durant le projet en mode Agile

3 sprints sont prévus
| _**Sprint**_           | **Sprint 1 : Analyse et initialisation**              | **Sprint 2 : Développement et configuration**          | **Sprint 3 : Backend et finalisation**                  |
|----------------------|-------------------------------------------------------|-------------------------------------------------------|---------------------------------------------------------|
| _**Rôles**_            |                                                       |                                                       |                                                         |
| Product Owner        | Frédéric                                               | Dylan                                                 | Fabrice                                                  |
| Scrum Master         | Dylan                                                  | Fabrice                                               | Frédéric                                                 |
| Développeur          | Fabrice                                                | Frédéric                                              | Dylan                   
| _**Objectifs**_        |                                                       |                                                       |                                                  |
|                      | - Analyse et compréhension du projet | - Continuer la configuration de l'environnement        |                      |
|                       | - Analyse du logiciel "KeyPass"      | - Création d'un nouvel utilisateur client pour tester la base de données | |
|                       | - Préparation du squelette des documents | - Finaliser la documentation "install.md" et "user_guide" |        |
|                       | - Mise en place de la VM et de Windows | - Batterie de tests "list test"                        |                      |
|                      |                                                       |                                                   |

## Choix techniques pour la maquette

#### - Le serveur est sous **Windows Server 2022**.
#### - Un des clients est sous **Windows 10 Pro**.
#### - Un autre client est sous **Ubuntu 24.04 LTS**.
#### - La version de **Keypass** utilisée est **2.57.1**.

## Difficultés / Solutions

#### - **Difficulté :** Gestion des droits d'accès utilisateurs au répertoire contenant la base de données sur le serveur.
#### - **Solution :** Utiliser un annuaire via le rôle/service **Active Directory** sur le serveur pour mieux gérer les droits d'accès.

## Suggestions d'améliorations

#### - Intégrer **Active Directory** pour une meilleure gestion des droits d'accès.
#### - Créer un **serveur de partage de fichiers** pour faciliter l'échange des bases de données KeyPass entre les utilisateurs.

## Bilan / Synthèse

#### - Aucun problème majeur n'a été rencontré durant cet exercice, malgré quelques difficultés liées à la gestion des droits de partage.
