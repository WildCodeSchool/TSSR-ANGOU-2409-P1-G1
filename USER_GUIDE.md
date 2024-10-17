# _**GUIDE DE L'UTILISATEUR [KEEPASS](https://keepass.info)**_ 

  ![Image logo keepass from Wikipedia](https://upload.wikimedia.org/wikipedia/commons/thumb/0/07/KeePass_Logo_%282016%29.svg/langfr-110px-KeePass_Logo_%282016%29.svg.png)

## Comment utiliser KEYPASS ##

### 1) Accès à l'application
  
   l'installation de Keepass est faite en local sur chaque poste de l'entreprise.
   l'application, dont l'icone ressemble au logo ci dessus et se nomme Keypass2,  se trouve dans le menu Démarrer dans la liste des programmes du poste de travail et sur le bureau de votre ordinateur.
   La stratégie informatique de l'entreprise permet de créer automatiquement l'icone de l'application sur le bureau de l'utilisateur lors de sa première connexion.

### 2) L'interface de Keepass

 
   A gauche de l'interface, il est possible de ranger ses mots de passe dans différents chapitres, par exemple "Internet" pour les comptes et mots de passe liés à un site web.
   A droite, les différentes entrées, sur différentes lignes, contenant un login et un mot de passe, éventuellement des remarques et d'autres paramètres comme le lien vers le site web par exemple.
   
   ![Image keepass from Google Drive](https://drive.google.com/thumbnail?id=1QCBhXlu0WrmuYdOCHxMCL-Td4qOKwZID&sz=w1000 "l'interface de Keepass")
   
   
### 3) Utilisation de Keepass
   
#### a) Ouvrir une base de données existante, soit en local soit sur le repertoire partagé dédié à Keepass sur le serveur SRVWIN01 de l'entreprise \SRVWIN01\Base Keepass Utilisateurs\
   
   Pour accéder facilement à ce repertoire, un raccourcis est disponible sur le bureau de votre ordinateur
   
   ![Image](https://drive.google.com/thumbnail?id=15Okbp-tWc3vXtqRvKg6pk8MEJZxY9vTI&sz=w1000 "Raccourci vers base keepass utilisateurs sur le serveur SRVWIN01")
   
   Ce raccourcis ouvre le repertoire contenant la base Keepass utilisateurs

![Image](https://drive.google.com/thumbnail?id=1FysMkDPz0jko3SCGQhXj-y0rsPRuDtb0&sz=w1000 "Copie écran repertoire contenant la base Keepass utilisateurs") 

Après un double clic sur le fichier .KDBX de la base utilisateurs, Keepass se lance et demande le **mot de passe maître** afin d'accéder au contenu de la base de données (Les 3 petits points à droite du champs de saisi permet de voir le mot de passe entré) 
    
  ![Image](https://drive.google.com/thumbnail?id=12eFCp1rrOZFM9fD8tshOKg3t0zASSv56&sz=w1000 "Ouvrir la base de données avec master key")
  
   #### b) Créer une nouvelle base de données pour une utilisation personnelle sur son poste de travail

   Ouvrir l'application Keepass et selectionner _File/New_

   ![Image](https://drive.google.com/thumbnail?id=1qluL5oo-ZQ8n-vLHorOlrHbnqhPLHIA0&sz=w1000 "Create database 1")

  L'application nous informe qu'il est fortement recommandé de régulièrement faire une sauvegarde de sécurité du fichier .KDBX et qu'il faudra bien se souvenir de l'endroit ou l'on sauvegarde ce fichier, évidemment !!! 😊
   
   ![Image](https://drive.google.com/thumbnail?id=1zdZ5OyO_Rao2TBIfQYb19aZcILITzW92&sz=w1000 "Create database 2")

   Spécifiez un nom et un emplacement pour votre base .KDBX
   ![Image](https://drive.google.com/thumbnail?id=19U5qku5jyNLaPXfKVDk4YH9VtYHo6AKo&sz=w1000 "Emplacemement database")
  
La création d'une base Keepass s'accompagne de la création d'un mot de passe maître pour l'accès à cette base. Il est possible de d'ouvrir un panneau d'option avec "Show Expert Options". Dans ces options, il est possible de durcir l'accès a votre base avec Key File, mais ce n'est pas obligatoire. Nous reviendrons dessus dans le chapitre "Uutilisation avancé de Keepass".
⚠️ Il est FORTEMENT DECONSEILLE de selectionner "Windows User Account" car votre base sera alors trop fortement lié à votre compte Windows. Catastrophique en cas de suppression de votre compte Windows.

![Image](https://drive.google.com/thumbnail?id=1_zYvPLGpatuxyX16fkNGgHzj2FG_CuoO&sz=w1000 "Create Master Key")

   L'application vous prévient si le mot de passe rentré est faible. 
   
 ![Image](https://drive.google.com/thumbnail?id=1DmevZG-uNMomAlK75WEZv1J55SDAR-sP&sz=w1000 "Master Key Weak")
   
      
- Bonnes pratiques pour la création d'un mot de passe
- Pour l'exemple, 2 entrées sont présentes par défaut lors de la création de la base et peuvent être supprimé sans problème.
   
4) Nouvelle entrée dans la base
   
     - Ajout d'un login et d'un mot de passe pour un compte, un site web
     - Supression d'une entrée dans la base
     - Génération automatique d'un mot de passe sécurisée
  
5) Focus sur les mots de passe sauvegardés dans la base

   IMPORTANT : Il est possible que vous soyez amené à changer votre mot de passe ou votre identifiant sur
l’un(e) de vos comptes/applications. Dans ce cas, il est __impératif__ d‘effectuer ce changement
également dans votre base de données KeePass (Ne pas oublier d’enregistrer).
       
6) Sauvegarde de la base de données

   - Copie du fichier .KBX qui est le fichier contenant la BD de mots de passe
   - Conseil sur la méthode de sauvegarde du .KDBX (Méthode 3/2/1)
   - Le fichiers Base Utilisateurs.KBX, est la base de données des mot de passe communs aux salariés sur le réseau de l'entreprise. Il est sécurisé avec une protection en écriture/supression pour un utilisateur standard.
     La base administrateur ne doit pas être  visible pour l'utilisateur standard (A METTRE DANS DOC ADMIN)
     La base utilisateur est accessible à tous les salariés. Contacter le service IT afin d'obtenir le mot de passe maître.
 
   
7) Utilisation de Keepass avec auto completion du login et du mot de passe.
   Cette fonctionnalité se nomme Auto-Type et le raccourci clavier par défaut est : Ctrl+V
   Utilisable pour par exemple :
   
   Un compte Windows, une application, un service web...
     

  

8) Utilisation avancée

   - Plugins-> notice admin ?
   - Raccourcis
   - Utilisation de la base de données depuis plusieurs appareils
   
10) FAQ

  Ma base de données Keepass est corrompu, que faire ? Contacter votre service IT
  
  Après installation de Keepass la langue utilisé est l'Anglais, alors que j'avais séléctionné Français. Que faire pour avoir   l'interface en Français ? => A mettre dans la doc Admin?

  Ou dois je sauvegarder ma base de données ? Il est conseillé de sauvegarder votre fichier .KBX dans le  repertoire réseau
  *E:\Base Keepass Utilisateurs\Autres utilisateurs*. En cas de supression accidentelle de votre base, le service informatique sera capable de restaurer votre fichier a une version antérieure.
  
  






