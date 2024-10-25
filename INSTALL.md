# **Gestion Base De Données Sécurisée De Mots De Passe**

## Guide d'installation et de paramétrage

### Prérequis pour les machines

| Machine          | Système d'exploitation      | Processeur              | Mémoire RAM        | Espace disque          | Connexion réseau               |
|------------------|-----------------------------|-------------------------|--------------------|------------------------|---------------------------------|
| **Client**       | Windows 10 Pro              | Intel / AMD | 4 Go minimum       | 20 Go d'espace libre   | Accès réseau filaire ou Wi-Fi  |
| **Serveur**       | Windows Server              | Intel / AMD | 8 Go minimum    | 40 Go d'espace libre   | Connexion réseau filaire        |
| **KeePass**      | Windows 10 Pro ou Server    | Processeur standard      | 4 Go minimum       | 100 Mo pour KeePass    | Accès à Internet pour les mises à jour |
<details>
<summary><strong>1) Configuration des utilisateurs et des machines
</strong></summary>


  <details>
  <summary>1.1 Renommer les machines client/serveur
  </summary>
 
##### 1.1.1 Client
Nous partons du principe que le système d'exploitation est déjà installé, dans notre cas Windows 10 PRO. 

Pour renommer votre client :
1. Rendez-vous dans **Paramètres** > **Système** > **À propos de**.
2. Cliquez sur "Renommer ce PC".
3. Dans notre cas, nous allons renommer la machine en `CLIWIN01`.

##### 1.1.2 Serveur
Le processus est similaire pour le serveur. Dans notre cas, nous utilisons Windows Server 2022, que nous allons renommer en `SRVWIN01`.

<img src="https://github.com/WildCodeSchool/TSSR-ANGOU-2409-P1-G1/blob/Images/Capture%20d'%C3%A9cran%202024-10-23%20144413.png?raw=true" width="300" height="300">

<img src="https://github.com/WildCodeSchool/TSSR-ANGOU-2409-P1-G1/blob/Images/Capture%20d'%C3%A9cran%202024-10-23%20145702.png?raw=true" width="500" height="300">


  </details>
  
  <details>
  <summary>1.2 Création d'un utilisateur "Wilder" dans le groupe des administrateurs locaux
  </summary>

##### 1.2.1 Sur le client (Windows 10 PRO)

Pour créer un utilisateur nommé ```Wilder``` et l'ajouter au groupe des administrateurs locaux, suivez les étapes suivantes :

1. **Accéder à la gestion des comptes** :
   - Ouvrez le **Panneau de configuration**.
   - Cliquez sur **Comptes d'utilisateurs**, puis sur **Gérer un autre compte**.
   - Sélectionnez **Ajouter un utilisateur à ce PC**.

2. **Ajouter un utilisateur** :
   - Sélectionnez l'option **Je ne dispose pas des informations de connexion de cette personne**.
   - Cliquez ensuite sur **Ajouter un utilisateur sans compte Microsoft**.

3. **Créer un compte local** :
   - Dans la fenêtre suivante, entrez le nom d'utilisateur ```Wilder```, un mot de passe (facultatif), et suivez les instructions pour terminer la création.

4. **Ajouter ```Wilder``` au groupe des administrateurs** :
   - Une fois l'utilisateur "Wilder" créé, ouvrez le **Menu Démarrer** et recherchez **Invite de commandes**. Faites un clic droit et sélectionnez **Exécuter en tant qu'administrateur**.
   - Dans l'invite de commandes, entrez la commande suivante pour ajouter ```Wilder``` au groupe des administrateurs locaux :
     ```bash
     net localgroup administrateurs Wilder /add
     ```

5. **Vérification** :
   - Pour vérifier que ```Wilder``` fait bien partie du groupe des administrateurs, tapez la commande suivante :
     ```bash
     net localgroup administrateurs
     ```

   - Vous devriez voir ```Wilder``` dans la liste des administrateurs.

##### 1.2.2 Sur le serveur (Windows Server 2022)

Le processus est similaire sur le serveur :
1. Ouvrez le **Gestionnaire de serveur**.
2. Cliquez sur **Outils** > **Gestion de l'ordinateur**.
3. Accédez à **Utilisateurs et groupes locaux** > **Utilisateurs**.
4. Faites un clic droit dans l'espace vide, puis sélectionnez **Nouvel utilisateur**.
5. Remplissez les informations pour l'utilisateur "Wilder".
6. Une fois l'utilisateur créé, ajoutez-le au groupe des administrateurs locaux :
   - Cliquez sur **Groupes**, puis faites un double-clic sur **Administrateurs**.
   - Ajoutez l'utilisateur "Wilder" au groupe.
  </details>

  <details>
  <summary>1.3 Mise en place du dossier partagé sur le serveur
  </summary>

1. Faites un clic droit sur le dossier contenant la base de données de KeePass.
2. Allez dans `Propriétés > Partager > icône Partager`, puis sélectionnez les utilisateurs avec lesquels vous souhaitez partager le dossier et gérez leurs droits
d'accès. Enfin, cliquez sur `Partager`.

<img src="https://github.com/WildCodeSchool/TSSR-ANGOU-2409-P1-G1/blob/Images/Capture%20d'%C3%A9cran%202024-10-25%20120038.png?raw=true" width="250" height="250">

---------------------------------------------------------------------------------------------

<img src="https://github.com/WildCodeSchool/TSSR-ANGOU-2409-P1-G1/blob/Images/Capture%20d'%C3%A9cran%202024-10-25%20120059.png?raw=true" width="250" height="250">

   **ATTENTION :** Les options de droits d'accès sur Windows sont puissantes. Par exemple, **Modifier** permet aux utilisateurs d'écrire et de supprimer des fichiers. Pour une gestion des droits plus fine et pour éviter les erreurs, il est recommandé d'utiliser l'Active Directory.
   
  </details>
  
</details> 
<details>
<summary><strong>2) Configuration des adresses IP pour un réseau local (Windows 10 Pro et Windows Server)
</strong></summary>
  
#### Configuration des adresses IP statiques sur le serveur Windows Server :

<img src="https://github.com/WildCodeSchool/TSSR-ANGOU-2409-P1-G1/blob/Images/Capture%20d'%C3%A9cran%202024-10-18%20113300.png?raw=true" width="500" height="300">

1. **Ouvrir les paramètres réseau** :

<img src="https://github.com/WildCodeSchool/TSSR-ANGOU-2409-P1-G1/blob/Images/Capture%20d'%C3%A9cran%202024-10-18%20113408.png?raw=true" width="500" height="300">

   - Accédez à **Panneau de configuration** > **Réseau et Internet** > **Centre Réseau et partage** > **Modifier les paramètres de la carte**.


<img src="https://github.com/WildCodeSchool/TSSR-ANGOU-2409-P1-G1/blob/Images/Capture%20d'%C3%A9cran%202024-10-18%20113418.png?raw=true" width="500" height="300">

     
   - Faites un clic droit sur la carte réseau > **Propriétés**.

<img src="https://github.com/WildCodeSchool/TSSR-ANGOU-2409-P1-G1/blob/Images/Capture%20d'%C3%A9cran%202024-10-18%20113615.png?raw=true" width="350" height="400">
    
   - Sélectionnez **Protocole Internet version 4 (TCP/IPv4)** et cliquez sur **Propriétés**.

<img src="https://github.com/WildCodeSchool/TSSR-ANGOU-2409-P1-G1/blob/Images/Capture%20d'%C3%A9cran%202024-10-18%20113638.png?raw=true" width="350" height="400">
  
2. **Entrer les paramètres d'adresse IP** :
  
<img src="https://github.com/WildCodeSchool/TSSR-ANGOU-2409-P1-G1/blob/Images/Capture%20d'%C3%A9cran%202024-10-18%20113557.png?raw=true" width="350" height="400">

   - Entrez une adresse IP statique, par exemple :
     - **Adresse IP** : `172.16.10.10`
     - **Masque de sous-réseau** : ```255.255.255.0```
     - **Passerelle par défaut** : ```172.16.10.254```
     - **DNS préféré** : ```172.16.10.10```
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
     ping 172.16.10.30
     ```
   - Si la configuration est correcte, vous verrez des réponses indiquant que les paquets sont transmis avec succès.

2. **Tester la connexion du client au serveur** :
   - Ouvrez une fenêtre de commande sur le client et tapez :
     ```
     ping 172.16.10.10
     ```
</details>

<details>
<summary><strong>3) Installation et configuration de KeePass
</strong></summary>

#### Étape 1 : Télécharger KeePass

Rendez-vous sur le site [KeePass](https://keepass.info) pour télécharger la version **2.57.1** de KeePass (dans notre cas).

#### Étape 2 : Lancer l'installation

1. Exécutez le programme d'installation.
2. Choisissez la langue **française** pour l'installation.
3. Acceptez les **Conditions Générales d'Utilisation (CGU)**.
   ![ce1](https://github.com/WildCodeSchool/TSSR-ANGOU-2409-P1-G1/blob/Images/Capture%20d'%C3%A9cran%202024-10-16%20143004.png?raw=true)
4. Sélectionnez le **chemin d'accès** où KeePass sera installé.
   ![ce2](https://github.com/WildCodeSchool/TSSR-ANGOU-2409-P1-G1/blob/Images/Capture%20d'%C3%A9cran%202024-10-16%20143036.png?raw=true)
5. Laissez les options par défaut pour les composants à installer, puis cliquez sur **Suivant**.
   ![ce3](https://github.com/WildCodeSchool/TSSR-ANGOU-2409-P1-G1/blob/Images/Capture%20d'%C3%A9cran%202024-10-16%20143059.png?raw=true) 
6. À l'étape des **tâches supplémentaires**, cochez simplement l'option pour **créer un raccourci sur le bureau**.
   ![ce4](https://github.com/WildCodeSchool/TSSR-ANGOU-2409-P1-G1/blob/Images/Capture%20d'%C3%A9cran%202024-10-16%20143112.png?raw=true) 
8. Si tout vous semble correct, lancez l'installation.
   ![ce5](https://github.com/WildCodeSchool/TSSR-ANGOU-2409-P1-G1/blob/Images/Capture%20d'%C3%A9cran%202024-10-16%20143131.png?raw=true)
   ![ce6](https://github.com/WildCodeSchool/TSSR-ANGOU-2409-P1-G1/blob/Images/Capture%20d'%C3%A9cran%202024-10-16%20143156.png?raw=true)
   ![ce7](https://github.com/WildCodeSchool/TSSR-ANGOU-2409-P1-G1/blob/Images/Capture%20d'%C3%A9cran%202024-10-16%20143220.png?raw=true)
#### Étape 3 : Finalisation

Après l'installation, une fenêtre vous demandera d'**activer la vérification automatique des mises à jour**. Sélectionnez **Enable** pour activer 
cette option.
![ce8](https://github.com/WildCodeSchool/TSSR-ANGOU-2409-P1-G1/blob/Images/Capture%20d'%C3%A9cran%202024-10-16%20143237.png?raw=true)

Félicitations, KeePass est prêt à être utilisé !
</details>

<details>
<summary><strong>4) Configuration des utilisateurs dans KeePass
</strong></summary>

1. **Ouvrir KeePass** : Lancez KeePass et accédez à votre base de données de mots de passe.

2. **Créer un nouvel utilisateur** :
   - Cliquez sur l'icône **Ajouter une entrée** (ou utilisez le raccourci `Ctrl + I`).
   - Remplissez les champs :
     - **Titre** : Le nom ou l'identifiant de l'utilisateur.
     - **Nom d'utilisateur** : L'identifiant utilisé pour la connexion.
     - **Mot de passe** : Créez un mot de passe sécurisé ou laissez KeePass en générer un automatiquement.
   - Optionnel : Ajoutez des informations complémentaires telles qu'une URL ou des notes.

3. **Enregistrer l'entrée** : Cliquez sur **OK** pour enregistrer le nouvel utilisateur.

</details>

<details>
<summary><strong>6) Mettre KeePass en français
</strong></summary>

1. Téléchargez le fichier ZIP depuis le site [KeePass Translations](https://keepass.info/translations.html).  
2. Depuis votre explorateur de fichiers, décompressez le fichier ZIP et copiez le fichier `French.lngx`.

   <img src="https://github.com/WildCodeSchool/TSSR-ANGOU-2409-P1-G1/blob/Images/Capture%20d'%C3%A9cran%202024-10-24%20101033.png?raw=true" width="500" height="300">
   
   <img src="https://github.com/WildCodeSchool/TSSR-ANGOU-2409-P1-G1/blob/Images/Capture%20d'%C3%A9cran%202024-10-24%20101058.png?raw=true" width="500" height="300">

3. Maintenant, rendez-vous dans votre disque `C:/`, puis dans `Programmes > KeePass Password Safe 2 > Languages`.
---
   <img src="https://github.com/WildCodeSchool/TSSR-ANGOU-2409-P1-G1/blob/Images/Capture%20d'%C3%A9cran%202024-10-24%20101138.png?raw=true" width="500" height="300">

---   
   <img src="https://github.com/WildCodeSchool/TSSR-ANGOU-2409-P1-G1/blob/Images/Capture%20d'%C3%A9cran%202024-10-24%20101201.png?raw=true" width="500" height="300">

---
  <img src="https://github.com/WildCodeSchool/TSSR-ANGOU-2409-P1-G1/blob/Images/Capture%20d'%C3%A9cran%202024-10-24%20101212.png?raw=true" width="500" height="300">

---
  <img src="https://github.com/WildCodeSchool/TSSR-ANGOU-2409-P1-G1/blob/Images/Capture%20d'%C3%A9cran%202024-10-24%20101225.png?raw=true" width="500" height="300">

---
  <img src="https://github.com/WildCodeSchool/TSSR-ANGOU-2409-P1-G1/blob/Images/Capture%20d'%C3%A9cran%202024-10-24%20101245.png?raw=true" width="500" height="300">


4. Ouvrez KeePass, puis allez dans `View > Change Language` et sélectionnez **Français** comme langue. KeePass vous demandera de redémarrer, cliquez sur **OK**.

   <img src="https://github.com/WildCodeSchool/TSSR-ANGOU-2409-P1-G1/blob/Images/Capture%20d'%C3%A9cran%202024-10-24%20101313.png?raw=true" width="500" height="300">
---
   <img src="https://github.com/WildCodeSchool/TSSR-ANGOU-2409-P1-G1/blob/Images/Capture%20d'%C3%A9cran%202024-10-24%20101320.png?raw=true" width="500" height="300">
---   

</details>

<details>
<summary><strong>5) Important : Sauvegarde de la base de données et Journalisation 
</strong></summary>

1.1 Il est crucial de faire des sauvegardes régulières de votre base de données KeePass. Nous recommandons d'utiliser la **méthode 3-2-1** :

1. **3 copies** de votre base de données (1 copie principale et 2 sauvegardes).
2. **2 types de stockage** différents (par exemple, un disque local et un stockage cloud).
3. **1 copie** située hors site (par exemple, sur un disque dur externe ou un serveur distant).

1.2 Mettre en place une journalisation de la base de données 3 fois par jour

1. **Configurer les Clichés instantanés ou la journalisation de la sauvegarde de la base KeePass** :
   - Commencez par activer la fonctionnalité des Clichés instantanés sur le disque qui contient la base de données KeePass.
  
  
     <img src="https://github.com/WildCodeSchool/TSSR-ANGOU-2409-P1-G1/blob/Images/cep1.jpg?raw=true" width="300" height="300">

---

2. **Les Clichés instantanés sont activés sur le disque E: qui contient la base KeePass** :
   - Assurez-vous que le disque contenant la base KeePass, dans cet exemple `E:`, a bien la fonctionnalité des Clichés instantanés activée.

     <img src="https://github.com/WildCodeSchool/TSSR-ANGOU-2409-P1-G1/blob/Images/cep2.jpg?raw=true" width="300" height="300">

---

3. **Paramètres et planification des clichés instantanés** :
   - Configurez la planification des Clichés instantanés pour qu'ils se déclenchent 3 fois par jour à des heures spécifiques (par exemple, à 8h, 12h et 18h).
       

     <img src="https://github.com/WildCodeSchool/TSSR-ANGOU-2409-P1-G1/blob/Images/cep3.jpg?raw=true" width="300" height="300">

  ---

  4. **Restaurer une version précédente d'un fichier** :
   - Pour restaurer une version précédente de la base de données KeePass, faites un clic droit sur le fichier concerné, puis sélectionnez **Restaurer les              versions précédentes**.

     <img src="https://github.com/WildCodeSchool/TSSR-ANGOU-2409-P1-G1/blob/Images/ce4.jpg?raw=true" width="300" height="300">
---

**Conseil** : Utilisez un **disque RAID** pour sécuriser davantage vos sauvegardes.
</details>

<details>
<summary><strong>FAQ
</strong></summary>

<details>
<summary><strong>Comment puis-je récupérer mon mot de passe principal si je l'oublie ?
</strong></summary>  
Malheureusement, il n'est pas possible de récupérer un mot de passe principal oublié dans KeePass. Assurez-vous de bien le mémoriser ou de le noter en lieu sûr.
</details>

<details>
<summary><strong>KeePass propose-t-il la synchronisation automatique entre plusieurs appareils ?
</strong></summary>
Non, KeePass ne dispose pas de cette fonctionnalité intégrée. Cependant, vous pouvez utiliser des services de cloud comme Google Drive ou Dropbox pour synchroniser manuellement votre fichier de base de données.
</details>

<details>
<summary><strong> Puis-je utiliser KeePass sur mon téléphone ?
</strong></summary>
Oui, KeePass dispose de versions mobiles, comme KeePassDroid pour Android ou Strongbox pour iOS, qui vous permettent d'accéder à votre base de données sur votre téléphone.
</details>

<details>
<summary><strong>Comment configurer KeePass pour une utilisation en réseau ?
</strong></summary>  
Placez la base de données sur un serveur sécurisé, avec un accès contrôlé par un partage réseau restreint.
Activez la fonctionnalité de synchronisation pour que plusieurs utilisateurs puissent travailler en parallèle sans conflit.
Utilisez un VPN pour les connexions distantes afin de protéger l'accès réseau à KeePass.
</details>

<details>
<summary><strong>Comment gérer les mises à jour de KeePass et des plug-ins ?
</strong></summary>
Téléchargez les mises à jour depuis le site officiel de KeePass pour éviter les versions altérées.
Testez les mises à jour sur un environnement de test avant de les déployer en production.
Maintenez les plug-ins à jour pour éviter les vulnérabilités de sécurité et pour garantir la compatibilité.
</details>

</details>
