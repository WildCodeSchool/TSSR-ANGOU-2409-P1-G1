# _**GUIDE DE L'UTILISATEUR [KEEPASS](https://keepass.info)**_ 

  ![Image logo keepass from Wikipedia](https://upload.wikimedia.org/wikipedia/commons/thumb/0/07/KeePass_Logo_%282016%29.svg/langfr-110px-KeePass_Logo_%282016%29.svg.png)

## Comment utiliser KEYPASS ##

### 1) Accès à l'application
  
   l'installation de Keepass est faite en local sur chaque poste de l'entreprise.
   l'application, dont l'icone ressemble au logo ci dessus et se nomme Keypass2,  se trouve dans le menu Démarrer dans la liste des programmes du poste de travail et sur le bureau de votre ordinateur.
   La stratégie informatique de l'entreprise permet de créer automatiquement l'icone de l'application sur le bureau de l'utilisateur lors de sa première connexion.

### 2) L'interface de Keepass

 
   A gauche de l'interface, il est possible de ranger ses mots de passe dans différents sous dossier de la base de données, par exemple "Internet" pour les comptes et mots de passe liés à un site web.
   A droite, les différentes entrées, sur différentes lignes, contenant un nom de préférence explicite, un login et un mot de passe, éventuellement des remarques et d'autres paramètres comme le lien vers le site web par exemple.
   
   ![Image keepass from Google Drive](https://drive.google.com/thumbnail?id=1QCBhXlu0WrmuYdOCHxMCL-Td4qOKwZID&sz=w1000 "l'interface de Keepass")
   
   
### 3) Utilisation de Keepass

Point important, par défaut KeePass ouvrira la dernière base de données utilisée mais pour ouvrir une autre base de données existante, cliquez sur _"Fichier"_, _"Ouvrir"_, et sélectionnez le fichier .kdbx qui correspond à la base de données dont vous souhaitez avoir accès.
   
#### a) Ouvrir une base de données existante, soit en local soit sur le repertoire partagé dédié à Keepass sur le serveur SRVWIN01 de l'entreprise \SRVWIN01\Base Keepass Utilisateurs\
   
   Pour accéder facilement au repertoire partagé sur le serveur, un raccourcis est disponible sur le bureau de votre ordinateur
   
   ![Image](https://drive.google.com/thumbnail?id=15Okbp-tWc3vXtqRvKg6pk8MEJZxY9vTI&sz=w1000 "Raccourci vers base keepass utilisateurs sur le serveur SRVWIN01")
   
   Ce raccourcis ouvre le repertoire contenant la base Keepass utilisateurs

![Image](https://drive.google.com/thumbnail?id=1FysMkDPz0jko3SCGQhXj-y0rsPRuDtb0&sz=w1000 "Copie écran repertoire contenant la base Keepass utilisateurs") 

Après un double clic sur le fichier .KDBX de la base utilisateurs, Keepass se lance et demande le **mot de passe maître** afin d'accéder au contenu de la base de données (Les 3 petits points à droite du champs de saisi permet de voir le mot de passe entré) 
    
  ![Image](https://drive.google.com/thumbnail?id=12eFCp1rrOZFM9fD8tshOKg3t0zASSv56&sz=w1000 "Ouvrir la base de données avec master key")

  La base de données s'ouvre alors et vous donne accès à tous les mots de passe "Utilisateurs" de l'entreprise (notamment les PC liés aux machines de production de l'usine).
  
   #### b) Créer une nouvelle base de données pour une utilisation personnelle sur son poste de travail

   Dans ce cas d'une utilisation personelle, le plus simple est d’ajouter compte et mot de passe au moment où une interface, un site le demande.
   Pour cela il faut avoir créer sa base de données au préalable.

  Pour cela :

   Ouvrir l'application Keepass et selectionner _File/New_

   ![Image](https://drive.google.com/thumbnail?id=1qluL5oo-ZQ8n-vLHorOlrHbnqhPLHIA0&sz=w1000 "Create database 1")

  L'application nous informe qu'il est fortement recommandé de régulièrement faire une sauvegarde de sécurité du fichier .KDBX et qu'il faudra bien se souvenir de l'endroit ou l'on sauvegarde ce fichier, évidemment !!! 😊
   
   ![Image](https://drive.google.com/thumbnail?id=1zdZ5OyO_Rao2TBIfQYb19aZcILITzW92&sz=w1000 "Create database 2")

   Spécifiez un nom et un emplacement pour votre base .KDBX
   
   ![Image](https://drive.google.com/thumbnail?id=19U5qku5jyNLaPXfKVDk4YH9VtYHo6AKo&sz=w1000 "Emplacemement database")
  
La création d'une base Keepass s'accompagne de la création d'un mot de passe maître pour l'accès à cette base. Il est possible d'ouvrir un panneaux d'option avec "Show Expert Options". Dans ces options, il est possible de durcir l'accès a votre base avec un **Key File**, mais ce n'est pas obligatoire. Nous reviendrons dessus dans le chapitre "Uutilisation avancé de Keepass".

⚠️ Il est FORTEMENT DECONSEILLE de selectionner "Windows User Account" car votre base sera alors trop fortement lié à votre compte Windows. Catastrophique en cas de suppression de votre compte Windows.

![Image](https://drive.google.com/thumbnail?id=1_zYvPLGpatuxyX16fkNGgHzj2FG_CuoO&sz=w1000 "Create Master Key")

   L'application vous prévient alors si le mot de passe entré est faible. Il est plus que conseillé d'utiliser un mot de passe fort, c'est à dire complexe. 
   En cliquant sur ce lien vous aurez accès à un site qui peut vous aider à créer ce mot de passe  : 
   https://www.economie.gouv.fr/particuliers/creer-mot-passe-securise
   
 ![Image](https://drive.google.com/thumbnail?id=1DmevZG-uNMomAlK75WEZv1J55SDAR-sP&sz=w1000 "Master Key Weak")
   
  Il faut ensuite donner un nom à votre base de données

  ![Image](https://drive.google.com/thumbnail?id=1K45b_b8nvn4zjK40O9Zs5ptNPBsWZJaL&sz=w1000 "Database Setting")

  Félicitations, vous venez de créer votre 1ère base de données de mot de passe avec Keepass !!! 👏
 

Pas d'inquiétude, pour l'exemple, 2 entrées sont présentes par défaut lors de la création de la base et peuvent être supprimé sans problème.

   
### 4) Nouvelle entrée dans la base

   Dans Keepass, une entrée est une unité de stockage. Une entrée contient au minimum un titre et un mot de passe. Il est possible d’y associer : un identifiant d’utilisateur, une adresse et une description.

  Il est très facile de créer une nouvelle entrée.
  Soit avec un clic droit dans la colonne de droite puis selection de "Add Entry", soit grâce à l'icone du haut. Ou encore, Ctrl+i.

![Image](https://drive.google.com/thumbnail?id=1jRank-qdcmrhNfqIkeu-TAb5pzAl0TPe&sz=w1000 "Create Entry-1")

Renseigner les champs obligatoires. A ce moment il est possible de selectioner une autre icone qu'une clef pour symboliser l'entrée.

![Image](https://drive.google.com/thumbnail?id=1jTZXxzpz5M8nuNcAwrPWVagQlS1eNNhZ&sz=w1000 "Create Entry-3")

Si vous êtes en manque d'inspiration pour le mot de passe, il est possible d'avoir la génération automatique d'un mot de passe sécurisée.

![Image](https://drive.google.com/thumbnail?id=1N9z0Xk0fHJRMT8erx_QA58KuRqYBoUZN&sz=w1000 "Generate a Password")


Après validation, votre nouvelle entrée apparait dans la colonne de droite dans le chapitre choisi (Internet, Email, Windows, Network,...)
Ici, l'entrée a été mise à la racine de Database_Utilisateur1, mais il est possible de selectionner un chapitre au moment de la création de l'entrée

![Image](https://drive.google.com/thumbnail?id=1CYITzCKATuoN9svEgCqkbzQyPeKYESO0&sz=w1000 "Create Entry-4")


Il est encore plus simple de supprimer une entrée, il suffit de la selectionner et d'appuyer sur la touche "Suppr" de votre clavier.
La confirmation de la supression apparait alors. Après confirmation, l'entrée disparait et est envoyé dans la corbeille de Keepass si elle est active (C'est une option).

![Image](https://drive.google.com/thumbnail?id=1OqXDlGJ-eniS6rX6hmXx34YD3yA2XgbI&sz=w1000 "Create Entry-4")


### 5) Focus sur les mots de passe sauvegardés dans la base

 ⚠️  IMPORTANT : Il est possible que vous soyez amené à changer votre mot de passe ou votre identifiant sur
l’un(e) de vos comptes/applications/site web. Dans ce cas, il est __impératif__ d‘effectuer ce changement
également dans votre base de données KeePass (Ne pas oublier d’enregistrer).
       
### 6) Sauvegarde de la base de données

   - Copie du fichier .KBX qui est le fichier contenant la BD de mots de passe
   - Conseil sur la méthode de sauvegarde du .KDBX (Méthode 3/2/1)
   - Le fichiers Base Utilisateurs.KBX, est la base de données des mot de passe communs aux salariés sur le réseau de l'entreprise. Il est sécurisé avec une protection en écriture/supression pour un utilisateur standard.
     La base administrateur ne doit pas être  visible pour l'utilisateur standard (A METTRE DANS DOC ADMIN)
     La base utilisateur est accessible à tous les salariés. Contacter le service IT afin d'obtenir le mot de passe maître.
 

### 7) Utilisation de Keepass pour renseigner un login et un mot de passe avec le presse papier (Ctrl+C puis  Ctrl+v)

  ⚠️ Focus sur 12s max pour faire l'action Ctrl+C puis  Ctrl+v

   
### 8) Utilisation de Keepass our renseigner un login et un mot de passe avec auto completion.

   Cette fonctionnalité se nomme Auto-Type et le raccourci clavier par défaut est : Ctrl+V
   Utilisable pour par exemple :
   
   Un compte Windows, une application, un service web...
     

  

### 9) Utilisation avancée

   - Création de groupes
   - Plugins-> notice admin ?
   - Raccourcis clavier
   - Utilisation de la base de données depuis plusieurs appareils
   
### 10) FAQ

  Ma base de données Keepass est corrompu, que faire ? Contacter votre service IT
  
  Après installation de Keepass la langue utilisé est l'Anglais, alors que j'avais séléctionné Français. Que faire pour avoir   l'interface en Français ? => A mettre dans la doc Admin?

  Ou dois je sauvegarder ma base de données ? Il est conseillé de sauvegarder votre fichier .KBX dans le  repertoire réseau
  *E:\Base Keepass Utilisateurs\Autres utilisateurs* avec une copie en local sur votre ordinateur en cas d'indisponibilité du repertoire réseau.
  En cas de supression accidentelle de votre base, le service informatique sera capable de restaurer votre fichier à une version antérieure du fichier dans le repertoire réseau.



