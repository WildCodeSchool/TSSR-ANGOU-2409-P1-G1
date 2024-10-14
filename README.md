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

|                    | Sprint 1                                             | Sprint 2                                             | Sprint 3                 |        
|--------------------|------------------------------------------------------|------------------------------------------------------|--------------------------|
| **ÉQUIPE**                                                                                                                                                  |        
| Product Owner      | Frédéric                                             | Dylan                                                | Fabrice                  |        
| Scrum Master       | Dylan                                                | Fabrice                                              | Frédéric                 |        
| Dev                | Fabrice                                              | Frédéric                                             | Dylan                    |                                
| *Objectifs*       | - Analyse et Compréhension du Projet                 | - Continuer la configuration de l'environnement avec la création d'un nouvelle utilisateur client pour test un base de donnée Utilisateur      |  XXXXXXXXXXXXXXXXXXXXXX  | 
|                    | - Analyse et Compréhension du Logiciel "KeyPass"     | - Batterie de test "list test"           |  XXXXXXXXXXXXXXXXXXXXXX  |
|                    | - Préparation du squelette des différents documents  | - Finir la documentation "install.md et le " user_guide "  |  XXXXXXXXXXXXXXXXXXXXXX  |        
|                    | - Mise en place et en service de la VM et Windows    |                                                      |                          |                         


## Choix techniques pour la maquette

Le serveur est sous OS Windows Server 2022 

Un des clients est sous Windows 10 Pro

Un autre client est sous Ubuntu 24.04 LTS

La version de Keypass est 2.57.1

## Difficultés / Solutions

Une des difficulté est la gestion des droits d'accès utilisateurs au repertoire contenant la base de données sur le serveur.
Une solution serait d'utiliser un annuaire en utilisant le rôle/service Active Directory sur le serveur.

## Suggestions d'améliorations



## Bilan/synthèse
