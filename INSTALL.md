# _**Gestion Base De Données Securisée De Mots De Passes**_

Guide d'installation et de paramétrage

1) Prérequis
   - Virtualbox doit être installé sur une machine hôte et configuré pour que les VM soit sur un réseau local (Configuration/réseau/réseau interne)=>AJOUT COPIE D'ECRAN
   - Avoir téléchargé les ISO sur le site de MICROSOFT
   - Avoir telechargé le logiciel KEEPASS sur le site officiel (http://www.keepass.info)
   - Avoir créer les utilisateurs sur le serveur
   - Avoir créer le dossier partagé  pour la base Keepass
   - Windows Serveur version 2022 installé sur un serveur
   - Windows 10 Pro installé sur un poste client
   - Ubuntu  24.04 LTS installé sur un poste client
   - Mettre les étapes d'installation avec des copies d'écran

2) Configuration des utilisateurs
   - Copies d'écran des manipulations a faire pour créer les utilisateurs

4) Configuration des adresses IP pour un réseau local
   - Copies d'écran des manipulations a faire (dans Virtual box sur client et serveur)
     
6) Configuration du reseau local avec adresses IP fixe
   - copies d'écran des manipulations a faire pour rentrer les adresses IP 
   - Tests de fonctionnalités du réseau avec la commande Ping
   - Création des répertoires partagés

### 7) Installation et configuration de KeePass

#### Étape 1 : Télécharger KeePass

Rendez-vous sur le site [keePasse](https://keepass.info) pour télécharger la version **2.57.1** de KeePass (dans notre cas).

#### Étape 2 : Lancer l'installation

1. Exécutez le programme d'installation.
2. Choisissez la langue **française** pour l'installation.
3. Acceptez les **Conditions Générales d'Utilisation (CGU)**.
4. Sélectionnez le **chemin d'accès** où KeePass sera installé.
5. Laissez les options par défaut pour les composants à installer, puis cliquez sur **Suivant**.
6. À l'étape des **tâches supplémentaires**, cochez simplement l'option pour **créer un raccourci sur le bureau**.
7. Si tout vous semble correct, lancez l'installation.

#### Étape 3 : Finalisation

Après l'installation, une fenêtre vous demandera d'**activer la vérification automatique des mises à jour**. Sélectionnez **Enable** pour activer cette option.

Félicitations, KeePass est prêt à être utilisé !

  
8) IMPORTANT : Faire une sauvegarde régulière de la base de données avec la méthode 3/2/1 (Privilégier le stockage de la base sur un disque RAID)
   
8) FAQ
