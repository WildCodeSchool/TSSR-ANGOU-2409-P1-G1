# **Gestion Base De Données Sécurisée De Mots De Passe**

## Guide d'installation et de paramétrage

### 1) Installation et configuration de KeePass

#### Étape 1 : Télécharger KeePass

Rendez-vous sur le site [KeePass](https://keepass.info) pour télécharger la version **2.57.1** de KeePass (dans notre cas).

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

---

### 2) Configuration des adresses IP pour un réseau local (Windows 10 Pro et Windows Server)

#### Configuration des adresses IP statiques sur le serveur Windows Server :

1. **Ouvrir les paramètres réseau** :
   - Accédez à **Panneau de configuration** > **Réseau et Internet** > **Centre Réseau et partage** > **Modifier les paramètres de la carte**.
   - Faites un clic droit sur la carte réseau > **Propriétés**.
   - Sélectionnez **Protocole Internet version 4 (TCP/IPv4)** et cliquez sur **Propriétés**.
   
2. **Entrer les paramètres d'adresse IP** :
   - Entrez une adresse IP statique, par exemple :
     - **Adresse IP** : `172.16.10.10`
     - **Masque de sous-réseau** : `255.255.255.0`
     - **Passerelle par défaut** : `172.16.10.254`
     - **DNS préféré** : `172.16.10.10`
   - Cliquez sur **OK** pour valider les paramètres.

#### Configuration des adresses IP statiques sur le client Windows 10 Pro :

1. **Ouvrir les paramètres réseau** :
   - Accédez aux paramètres réseau comme pour Windows Server.

2. **Entrer les paramètres d'adresse IP** :
   - Entrez une adresse IP statique différente, par exemple :
     - **Adresse IP** : `172.16.10.30`
     - **Masque de sous-réseau** : `255.255.255.0`
     - **Passerelle par défaut** : `172.16.10.254`
     - **DNS préféré** : `172.16.10.10`

#### Tests de connectivité avec la commande `ping` :

1. **Tester la connexion du serveur au client** :
   - Ouvrez une fenêtre de commande (`cmd`) sur le serveur et exécutez la commande suivante :
     ```
     ping 192.168.1.20
     ```
   - Si la configuration est correcte, vous verrez des réponses indiquant que les paquets sont transmis avec succès.

2. **Tester la connexion du client au serveur** :
   - Ouvrez une fenêtre de commande sur le client et tapez :
     ```
     ping 192.168.1.10
     ```

---

### 3) Configuration des utilisateurs dans KeePass

1. **Ouvrir KeePass** : Lancez KeePass et accédez à votre base de données de mots de passe.

2. **Créer un nouvel utilisateur** :
   - Cliquez sur l'icône **Ajouter une entrée** (ou utilisez le raccourci `Ctrl + I`).
   - Remplissez les champs :
     - **Titre** : Le nom ou l'identifiant de l'utilisateur.
     - **Nom d'utilisateur** : L'identifiant utilisé pour la connexion.
     - **Mot de passe** : Créez un mot de passe sécurisé ou laissez KeePass en générer un automatiquement.
   - Optionnel : Ajoutez des informations complémentaires telles qu'une URL ou des notes.

3. **Enregistrer l'entrée** : Cliquez sur **OK** pour enregistrer le nouvel utilisateur.

---

### 4) Important : Sauvegarde de la base de données

Il est crucial de faire des sauvegardes régulières de votre base de données KeePass. Nous recommandons d'utiliser la **méthode 3-2-1** :

1. **3 copies** de votre base de données (1 copie principale et 2 sauvegardes).
2. **2 types de stockage** différents (par exemple, un disque local et un stockage cloud).
3. **1 copie** située hors site (par exemple, sur un disque dur externe ou un serveur distant).

**Conseil** : Utilisez un **disque RAID** pour sécuriser davantage vos sauvegardes.

---

### FAQ

#### Comment puis-je récupérer mon mot de passe principal si je l'oublie ?
Malheureusement, il n'est pas possible de récupérer un mot de passe principal oublié dans KeePass. Assurez-vous de bien le mémoriser ou de le noter en lieu sûr.

#### KeePass propose-t-il la synchronisation automatique entre plusieurs appareils ?
Non, KeePass ne dispose pas de cette fonctionnalité intégrée. Cependant, vous pouvez utiliser des services de cloud comme Google Drive ou Dropbox pour synchroniser manuellement votre fichier de base de données.

#### Puis-je utiliser KeePass sur mon téléphone ?
Oui, KeePass dispose de versions mobiles, comme KeePassDroid pour Android ou Strongbox pour iOS, qui vous permettent d'accéder à votre base de données sur votre téléphone.

