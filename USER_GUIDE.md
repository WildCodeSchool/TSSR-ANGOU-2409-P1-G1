# _**GUIDE DE L'UTILISATEUR [KEEPASS](https://keepass.info)**_ 

  ![Image logo keepass from Wikipedia](https://upload.wikimedia.org/wikipedia/commons/thumb/0/07/KeePass_Logo_%282016%29.svg/langfr-110px-KeePass_Logo_%282016%29.svg.png)

## Comment utiliser KEYPASS ##

### 1) Accès à l'application
  
   l'installation de Keepass est faite en local sur chaque poste de l'entreprise.
   l'application, dont l'icone ressemble au logo ci dessus se nomme __Keypass2__,  se trouve dans le menu Démarrer dans la liste des programmes du poste de travail et sur le bureau de votre ordinateur.
   La stratégie informatique de l'entreprise permet de créer automatiquement l'icone de l'application sur le bureau de l'utilisateur lors de sa première connexion.

### 2) L'interface de Keepass

 
   A gauche de l'interface, il est possible de ranger ses mots de passe dans différents sous dossier de la base de données, par exemple "Internet" pour les comptes et mots de passe liés à un site web.
   A droite, les différentes entrées, sur différentes lignes, contenant un nom de préférence explicite, un login et un mot de passe, éventuellement des remarques et d'autres paramètres comme le lien vers le site web par exemple.
   
   ![Image keepass from Google Drive](https://drive.google.com/thumbnail?id=1QCBhXlu0WrmuYdOCHxMCL-Td4qOKwZID&sz=w1000 "l'interface de Keepass")
   
   
### 3) Utilisation de Keepass

Point important, par défaut KeePass ouvrira la dernière base de données utilisée mais pour ouvrir une autre base de données existante, cliquez sur _"Fichier"_, _"Ouvrir"_, et sélectionnez le fichier .kdbx qui correspond à la base de données dont vous souhaitez avoir accès.
   
#### a) Ouvrir une base de données existante, soit en local soit sur le repertoire partagé dédié à Keepass sur le serveur SRVWIN01 de l'entreprise \SRVWIN01\Base Keepass Utilisateurs\
   
   Pour accéder facilement au repertoire partagé sur le serveur, un raccourcis est disponible sur le bureau de votre ordinateur.
   
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
  
La création d'une base Keepass s'accompagne de la création d'un mot de passe maître pour l'accès à cette base. Il est possible d'ouvrir un panneaux d'option avec "Show Expert Options". Dans ces options, il est possible de durcir l'accès a votre base avec un **Key File**, mais ce n'est pas obligatoire. Nous reviendrons dessus dans le chapitre "Utilisation avancé de Keepass".

⚠️ Il est FORTEMENT DECONSEILLE de selectionner "Windows User Account" car votre base sera alors trop fortement lié à votre compte Windows. Catastrophique en cas de suppression de votre compte Windows.

![Image](https://drive.google.com/thumbnail?id=1_zYvPLGpatuxyX16fkNGgHzj2FG_CuoO&sz=w1000 "Create Master Key")

   L'application vous prévient alors si le mot de passe entré est faible. Il est plus que conseillé d'utiliser un mot de passe fort, c'est à dire complexe. 
   En cliquant sur ce lien vous aurez accès à un site qui peut vous aider à créer ce mot de passe  : 
   https://www.economie.gouv.fr/particuliers/creer-mot-passe-securise
   
   ⚠️ Au moment de la création du mot de passe maître, Il est FORTEMENT CONSEILLE d'imprimer la "feuille de secours", la remplir, puis la stocker dans un endroit sécurisé, à l'abri des yeux indiscret. Dans un coffre fort pour une entreprise ou un tiroir qui ferme à clef pour un particulier.
   
 ![Image](https://drive.google.com/thumbnail?id=1DmevZG-uNMomAlK75WEZv1J55SDAR-sP&sz=w1000 "Master Key Weak")
   
  Il faut ensuite donner un nom à votre base de données

  ![Image](https://drive.google.com/thumbnail?id=1K45b_b8nvn4zjK40O9Zs5ptNPBsWZJaL&sz=w1000 "Database Setting")

  Félicitations, vous venez de créer votre 1ère base de données de mot de passe avec Keepass !!! 👏
 

Pas d'inquiétude, pour l'exemple, 2 entrées sont présentes par défaut lors de la création de la base et peuvent être supprimé sans problème.

   
### 4) Nouvelle entrée dans la base, supression d'une entrée

   Dans Keepass, une entrée est une unité de stockage. Une entrée contient au minimum un titre et un mot de passe. Il est possible d’y associer : un identifiant d’utilisateur, une adresse et une description.

  Il est très facile de créer une nouvelle entrée.
  Soit avec un clic droit dans la colonne de droite puis selection de "Add Entry", soit grâce à l'icone du haut. Ou encore, Ctrl+i.

![Image](https://drive.google.com/thumbnail?id=1jRank-qdcmrhNfqIkeu-TAb5pzAl0TPe&sz=w1000 "Create Entry-1")

Renseigner les champs obligatoires. A ce moment il est possible de selectioner une autre icone qu'une clef pour symboliser l'entrée pour une meilleure organisation visuelle dans la base.

![Image](https://drive.google.com/thumbnail?id=1jTZXxzpz5M8nuNcAwrPWVagQlS1eNNhZ&sz=w1000 "Create Entry-3")

Si vous êtes en manque d'inspiration pour le mot de passe, il est possible d'avoir la génération automatique d'un mot de passe sécurisée.

![Image](https://drive.google.com/thumbnail?id=1N9z0Xk0fHJRMT8erx_QA58KuRqYBoUZN&sz=w1000 "Generate a Password")


Après validation, votre nouvelle entrée apparait dans la colonne de droite dans le chapitre choisi (Internet, Email, Windows, Network,...)
Ici, l'entrée a été mise à la racine de Database_Utilisateur1, mais il est possible de selectionner un chapitre au moment de la création de l'entrée afin d'organiser au mieux ses entrées.

![Image](https://drive.google.com/thumbnail?id=1CYITzCKATuoN9svEgCqkbzQyPeKYESO0&sz=w1000 "Create Entry-4")


⚠️ N'oubliez pas de sauvegarder votre nouvelle entrée dans la base en appuyant sur l'icone "Disquette", ou par Ctrl+s.


Il est encore plus simple de supprimer une entrée, il suffit de la selectionner et d'appuyer sur la touche "Suppr" de votre clavier.
La confirmation de la supression apparait alors. Après confirmation, l'entrée disparait et est envoyé dans la corbeille de Keepass si elle est active (C'est une option).

![Image](https://drive.google.com/thumbnail?id=1OqXDlGJ-eniS6rX6hmXx34YD3yA2XgbI&sz=w1000 "Create Entry-4")


### 5) Focus sur les mots de passe sauvegardés dans la base

 ⚠️  IMPORTANT : Il est possible que vous soyez amené à changer votre mot de passe ou votre identifiant sur
l’un(e) de vos comptes/applications/site web. Dans ce cas, il est __impératif__ d‘effectuer ce changement
également dans votre base de données KeePass (Ne pas oublier d’enregistrer).
       
 

### 6) Utilisation de Keepass pour renseigner un login et un mot de passe avec le presse papier (Ctrl+C puis  Ctrl+v)

  L'interêt évident de Keepass et de pouvoir retrouver ses mots de passe facilement dans la base de données et pouvoir copier/coller le login et le mot de passe au bon endroit. C'est possible grâce au copier/coller (Ctrl+C puis  Ctrl+v) de Windows.

IMAGE

  ⚠️ ATTENTION, par défaut vous n'avez que 12 secondes pour faire l'action Ctrl+C puis Ctrl+v, car ensuite pour une question de sécurité, le presse papier est effacé !!!
  Ce temps est paramètrable dans les options de Keepass : 

  ![Image](https://drive.google.com/thumbnail?id=1hM6GfhAu2chkoUGN6bQ0ccOiNVv_L553&sz=w1000 "Paramètre 12s")

   
### 7) Utilisation de Keepass pour renseigner un login et un mot de passe avec auto completion.

   Cette fonctionnalité se nomme Auto-Type et le raccourci clavier par défaut est : Ctrl+V

  Ce raccourci est utilisable pour renseigner automatiquement le login et le mot de passe d'un compte Windows, une application, un service web,...
   
   Par exemple :  en ayant préalablement selectionné une entrée dans Keepass correspondant au login et MDP d'un site web, le raccourci Ctrl+u va permettre d'ouvrir la page web dans votre navigateur par défaut, puis la combinaison de touches Ctrl+v va remplir automatiquement les champs login et MDP en utilisant les informations que vous avez préalablement renseignées dans la base Keepass. 
   
Preselection de l'entrée qui vous interresse :

![Image](https://drive.google.com/thumbnail?id=1o052yUWgDQl_ZZ19dl-irOIXcryU9f3J&sz=w1000 "Preselection entrée")

Lorsque que Ctrl+u est pressé, ouverture de votre site web :

![Image](https://drive.google.com/thumbnail?id=1f0w8CQMJ4T96akMWvrTJrQIfFH3mkz_E&sz=w1000 "Preselection entrée")

Lorsque que ctrl+v est pressé, remplissage automatique du login, du mot de passe et ouverture de l'application :

![Image](https://drive.google.com/thumbnail?id=1WzJccgvIqmHKqEHNQhke5ew3tPGaptLS&sz=w1000 "Action Ctrl+v")

Et voilà le résultat :

![Image](https://drive.google.com/thumbnail?id=1vF6RTmZpK7qRX3nqOsSMYgIS-6VkjHwK&sz=w1000 "compte github ouvert depuis keepass")

  C'est pratique n'est ce pas ?


### 8) Accès aux bases de données Keepass de l'entreprise et sauvegarde de la base de données

Si votre base de données n'est pas mise dans un repertoire réseau sur le serveur SRVWIN01

   - il est vraiment nécessaire de faire une copie du fichier .KBX qui est le fichier contenant toutes vos entrées donc tous vos mots de passe.
   - Il est conseillé d'utiliser la méthode de sauvegarde 3/2/1
   - Le fichiers Base Utilisateurs.KBX, est la base de données des mot de passe communs aux salariés sur le réseau de l'entreprise. Il est sécurisé avec une protection en écriture/supression pour un utilisateur standard.
     La base administrateur n'est pas accessible à un utilisateur standard (A METTRE DANS DOC ADMIN)
     La base utilisateur est accessible à tous les salariés. Contacter le service IT afin d'obtenir le mot de passe maître.


### 9) Utilisation avancée

Les points abordés ci-dessus permettent d'utiliser Keepass pour une utilisation basique. Mais ce logiciel possède des fonctions avancées très interressantes comme par exemple :

   - Durcir la sécurité pour accéder à la base Keepass avec un fichier clef (double authentification 2FA)
   - Création de groupes
   - l'ajout de Plugins
   - De nombreux raccourcis clavier
   - Une utilisation de la base de données depuis plusieurs appareils (Avec sauvegarde de la base dans le cloud, mais attention ceci est parfois interdit par certaines entreprises ou organisations)

     N'hésitez pas à consulter la notice officielle Keepass pour ces fonctions avancées : https://keepass.info/features.html
   
### 10) FAQ

  Ma base de données Keepass est corrompu, que faire ? Contacter votre service IT pour restaurer une sauvegarde de la base.

  Les menus de Keepass sont en Anglais, est ce possible de les avoir en Français ? Contacter votre service IT afin d'installer le pack de langue Français (Parfois à l'installation du logiciel, même si le Français est selectionné, Keepass démarre en Anglais)

  Ou dois je sauvegarder ma base de données ? Il est conseillé de sauvegarder votre fichier .KBX dans un repertoire réseau sur le serveur SRVWIN01, par exmple dans  *E:\Base Keepass Utilisateurs\Autres utilisateurs* avec une copie en local sur votre ordinateur en cas d'indisponibilité du repertoire réseau.
  En cas de supression accidentelle de votre base, le service informatique sera capable de restaurer votre fichier à une version antérieure du fichier dans le repertoire réseau.

  J'ai perdu mon mot de passe maître pour avoir accès à ma base Keepass .KDBX, que faire ? Il faut espérer que vous ayez pris soin d'imprimer et rempli la "feuille de secours" Keepass lors de la création du mot de passe maître.
  



