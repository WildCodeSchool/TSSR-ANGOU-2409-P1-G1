![KEYPASS](https://img.linuxfr.org/img/68747470733a2f2f6b6565706173732e696e666f2f696d616765732f69636f6e732f6b6565706173735f333232783133322e706e67/keepass_322x132.png)

# _**Gestion Base De Données Securisée De Mots De Passe**_

# Documentation Générale

## Introduction

La gestion des mots de passe dans une entreprise est un enjeu crucial et souvent complexe. La sécurité d'un système d'information dépend en grande partie de la solidité de ces mots de passe. Cependant, les méthodes pour les pirater deviennent de plus en plus avancées. Il est essentiel d'encourager l'utilisation de mots de passe forts, mais cela se traduit souvent par la création de chaînes de caractères complexes, difficiles à retenir. Alors, comment peut-on assurer la sécurité tout en simplifiant la gestion de ces mots de passe ? Cherchons à répondre à cette question essentielle...

## Présentation du projet 

L'objectif de ce projet est de gérer, administrer et maintenir une base de données sécurisée de mots de passe en mode client/serveur. Cette base sera gérée à l'aide du logiciel KeePass et sera accessible à la fois aux administrateurs et aux utilisateurs du système d'information de l'entreprise.

La base de données dédiée aux administrateurs sera isolée de celle destinée aux utilisateurs, avec des répertoires partagés distincts, des droits d'accès différents et des clés d'accès spécifiques pour chaque groupe.

Concernant la sécurité de cette base, il faut savoir que depuis 2013 Keepass 2.x à été ajouté à la liste du socle interministériel de logiciels libres préconisés par l’État Français et la version 2.10 est certifiée par l'Agence nationale de la sécurité des systèmes d'information.


##  Mise en contexte

KeePass est un outil, sous licence GPL v2 ou ultérieure, qui permet non seulement la gestion sécurisée raisonnée et organisée des mots de passe, mais offre également de très pratiques raccourcis et autres facilités qui soulagent le quotidien.
La base de donnée de cet outil sera installé sur un serveur et accessible depuis n'importe quel poste et n'importe quel client connecté au réseau de l'entreprise.
Pour le projet, une maquette sera réalisé avec un serveur et un poste client dans un environnement Windows sur un réseau local avec des machines configuré avec des adresses IP fixes.
La méthode Agile sera utilisé pendant cette phase de developement.

## Rôles de chaque membre durant le projet en mode Agile

3 sprints sont prévus
| _**Sprint**_           | **Sprint 1 : Analyse et initialisation**              | **Sprint 2 : Développement et configuration**          | **Sprint 3 : Backend et finalisation**                  |
|----------------------|-------------------------------------------------------|-------------------------------------------------------|---------------------------------------------------------|
| _**Rôles**_            |                                                       |                                                       |                                                         |
| Product Owner        | Frédéric                                               | Dylan                                                 | Dylan                                                  |
| Scrum Master         | Dylan                                                  | Fabrice                                               | Frédéric                                                 |
| Développeur          | Fabrice                                                | Frédéric                                              |                    
| _**Objectifs**_        |                                                       |                                                       |                                                  |
|                      | - Analyse et compréhension du projet | - Continuer la configuration de l'environnement                          |  Finaliser la documentation                      |
|                       | - Analyse du logiciel "KeyPass"      | - Création d'un nouvel utilisateur client pour tester la base de données | Finaliser la maquette en prenant en compte le retours des tests               |
|                       | - Préparation du squelette des documents | - Finaliser la documentation "install.md" et "user_guide" |   Ajouter un client Ubuntu                                                     |
|                       | - Mise en place de la VM et de Windows | - Batterie de tests                         |                                                                               |
|                      |                                                       |                                                                                                           |




TABLEAU MIRO :
Cette application web nous a aidé à gérer notre projet en mode Agile

![KEYPASS](https://img.linuxfr.org/img/68747470733a2f2f6b6565706173732e696e666f2f696d616765732f69636f6e732f6b6565706173735f333232783133322e706e67/keepass_322x132.png)
https://drive.google.com/file/d/12fye1CKaDPv57CcqsqnG99A6VOhPyen3/view?usp=sharing



## Choix techniques pour la maquette

Nous avons considéré comme pré-requis la création des machines virtuelles sous Virtual Box et la configuration des cartes réseaux.
Mais la configuration des comptes demandés et les adresses IP est détaillé dans la documentation INSTALL.md

#### - Le serveur est sous **Windows Server 2022**. (VM sous Virtual Box avec utilisation du rôle serveur de stockage et la fonctionnalité partage SMB/CIFS pour l'accès depuis le client Ubuntu. Mise en place d'instantanées de sauvegarde sur un disque dédié pour la base Keepass)
#### - Un des clients est sous **Windows 10 Pro**. (VM sous Virtual Box)
#### - Un autre client est sous **Ubuntu 24.04 LTS**. (VM sous Virtual Box et installation de Samba pour l'accès au repertoire partagé du serveur sous Windows)
#### - La version de **Keepass** utilisée pour le client Windows est **2.57.1**. (Installation sur chaque postes Windows)
#### - KeepassXC 2.7.9 est utilisé pour le client Linux

IMPORTANT : Les bases de données sont compatible entre Keepass et KeepassXC

## Difficultés / Solutions

#### - **Difficulté :** Gestion des droits d'accès utilisateurs au répertoire contenant la base de données Administrateur sur le serveur.
#### - **Solution :** Journalisation de sauvegardes du disque contenant les repertoires partagés contenant les bases de données .kdbx de Keepass.

#### - **Autre difficulté :** L'accès au reperoire partagé du serveur Windows depuis le client Ubuntu. Il à été possible d'accéder au repertoire et à la base Keepass mais après redémarrage de la VM Ubuntu, le partage était perdu
#### - **Solution :** Effectué le montage au démarrage de la VM Ubuntu du/des repertoire(s) partagé(s) dans /mnt/Base_Keepass,  par exemple. Le montage devra être fait dans le repertoire /etc dans le fichier fstab

## Suggestions d'améliorations

#### - Déployer un controleur de domaine avec un annuaire **Active Directory** pour une meilleure gestion des droits d'accès.
#### - Créer des GPO sur le serveur pour automatiser la création des raccourcis du repertoire réseau partagé et icone de l'application Keepass sur le bureau d'un utilisateur lors de sa première connexion sur une machine lié au domaine


## Bilan

#### - Le plus gros problème rencontré durant ce projet à été la gestion des droits d'accès/modification de la base pour le groupe administrateur. Il nous à été impossible d'interdire la supression du fichier .KDBX sans supprimer le droit de modification (afin de pouvoir ajouter ou supprimer des entrées dans la base).
La supression accidentelle de la base par un administrateur pourra être réparé grace à la journalisation de la sauvegarde du repertoire réseau partagé.
3 sauvegardes par jours semble palier à ce problème (voir documentation INSTALL admin pour la configuration des instantanées) .


## Liens utiles

https://keepass.info/
https://fr.wikipedia.org/wiki/KeePass
https://cyber.gouv.fr/bonnes-pratiques-protegez-vous
https://www.it-connect.fr/comment-gerer-ses-mots-de-passe-avec-keepass-ou-keepassxc/
https://linuxfr.org/news/keepass-ou-apprendre-a-gerer-correctement-ses-mots-de-passe
https://siocours.lycees.nouvelle-aquitaine.pro/doku.php/systeme/authentification/keepass
https://www.motdepasse.xyz/

