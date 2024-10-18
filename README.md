![KEYPASS](https://img.linuxfr.org/img/68747470733a2f2f6b6565706173732e696e666f2f696d616765732f69636f6e732f6b6565706173735f333232783133322e706e67/keepass_322x132.png)

# _**Gestion Base De Données Securisée De Mots De Passes**_

# Documentation Générale

## Introduction

La gestion des mots de passe dans une entreprise est un enjeu crucial et souvent complexe. La sécurité d'un système d'information dépend en grande partie de la solidité de ces mots de passe. Cependant, les méthodes pour les pirater deviennent de plus en plus avancées. Il est essentiel d'encourager l'utilisation de mots de passe forts, mais cela se traduit souvent par la création de chaînes de caractères complexes, difficiles à retenir. Alors, comment peut-on assurer la sécurité tout en simplifiant la gestion de ces mots de passe ? Cherchons à répondre à cette question essentielle...

## Présentation du projet 

L'objectif de ce projet est de gérer, administrer et maintenir une base de données sécurisée de mots de passe en mode client/serveur. Cette base sera gérée à l'aide du logiciel KeePass et sera accessible à la fois aux administrateurs et aux utilisateurs du système d'information de l'entreprise.

La base de données dédiée aux administrateurs sera isolée de celle destinée aux utilisateurs, avec des répertoires partagés distincts, des droits d'accès différents et des clés d'accès spécifiques pour chaque groupe.

Concernant la sécurité de cette base, il faut savoir que depuis 2013 Keepass 2.x à été ajouté à la liste du socle interministériel de logiciels libres préconisés par l’État Français et la version 2.10 est certifiée par l'Agence nationale de la sécurité des systèmes d'information.


##  Mise en contexte

KeePass est un outil, sous licence GPL v2 ou ultérieure, qui permet non seulement la gestion raisonnée et organisée des mots de passe, mais offre également de très pratiques raccourcis et autres facilités qui soulagent le quotidien.
La base de donnée de cet outil sera installé sur un serveur et accessible depuis n'importe quel poste et n'importe quel client connecté au réseau de l'entreprise.
Pour le projet, une maquette sera réalisé avec un serveur et un poste client dans un environnement Windows sur un réseau local avec des machines configuré avec des adresses IP fixes.
La méthode Agile sera utilisé pendant cette phase de developement.

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

## Difficultés / Solutions - CHAPITRE A RETRAVAILLER

#### - **Difficulté :** Gestion des droits d'accès utilisateurs au répertoire contenant la base de données sur le serveur.
#### - **Solution :** Utiliser un annuaire via le rôle/service **Active Directory** sur le serveur pour mieux gérer les droits d'accès.

## Suggestions d'améliorations - CHAPITRE A RETRAVAILLER

#### - Déployer **Active Directory** pour une meilleure gestion des droits d'accès.
#### - Créer un **serveur de partage de fichiers** pour faciliter l'échange des bases de données KeyPass entre les utilisateurs.

## Bilan / Synthèse - CHAPITRE A RETRAVAILLER

#### - Aucun problème majeur n'a été rencontré durant cet exercice, malgré quelques difficultés liées à la gestion des droits de partage.
