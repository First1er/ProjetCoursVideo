# PROJET 1: ProjetCoursVideo
Ce projet vise à concevoir une sorte de lecteur vidéo en ligne dans le but d'apprendre de manière structurée.

## Rapport de mise en place de la Base de donnée

##   Nom de la Bd : NanVideoCourses
  Nous avons en tout conçu 9 tables tels que conçu:
  
##  Mois (
    - id INTEGER PRIMARY KEY AUTO_INCREMENT,
    - mois VARCHAR
  );
  
## categorieModule (
    - id INTEGER PRIMARY KEY AUTO_INCREMENT,
    - nom VARCHAR
  );
  
## user (
    - id INTEGER PRIMARY KEY AUTO_INCREMENT,
    - nom VARCHAR,
    - prenom VARCHAR,
    - email VARCHAR,
    - password VARCHAR
  );
  
## cours (
    - id INTEGER PRIMARY KEY AUTO_INCREMENT,
    - titre TEXT,
    - description TEXT,
    - #module_id INTERGER
  );
  
## module (
    - id INTEGER PRIMARY KEY AUTO_INCREMENT,
    - nom VARCHAR,
    - description TEXT,
    - duree_module DATE,
    - date_debut DATE,  # la date à laquelle l'utilisateur a commencé à suivre ce cours afin de recupérer le mois à partir de la fonction MONTH()
    - #id_categorie INTEGER,
    - #id_mois INTEGER
  );
  
## user_module (
    - #module_id INTEGER,
    - #user_id INTEGER
  );
    
## user_quiz (
    - #quiz_id INTEGER,
    - #user_id INTEGER
  );
  
## chapitre (
    - id INTEGER PRIMARY KEY AUTO_INCREMENT,
    - titre TEXT,
    - description TEXT,
    - #cours_id INTEGER
  );
  
## quiz (
    - id INTEGER PRIMARY KEY AUTO_INCREMENT,
    - titre TEXT,
    - #chapitre_id
  );
    
    
  ......................................................................................................................
  
  
# PROJET 2: E-commerceBd
  
  
##   Nom de la Bd : NanEcommerce
  Nous avons en tout conçu 13 tables tels que conçu:
  
##  genre (
    - id INTEGER PRIMARY KEY AUTO_INCREMENT,
    - nom_genre VARCHAR,
  );
  
## categorieProduit (
    - id INTEGER PRIMARY KEY AUTO_INCREMENT,
    - nom VARCHAR
  );
  
## Genre_categorie (
    - #categorie_id INTEGER,
    - #genre_id INTEGER
  );
  
## matiere (
    - id INTEGER PRIMARY KEY AUTO_INCREMENT,
    - nom_matière VARCHAR
  );
  
## marque (
    - id INTEGER PRIMARY KEY AUTO_INCREMENT,
    - nom_marque VARCHAR
  );
  
## couleur (
    - id INTEGER PRIMARY KEY AUTO_INCREMENT,
    - nom_couleur VARCHAR
  );
  
## taille (
    - id INTEGER PRIMARY KEY AUTO_INCREMENT,
    - taille VARCHAR
  );
  
## longeur (
    - id INTEGER PRIMARY KEY AUTO_INCREMENT,
    - long VARCHAR
  );
  
## media (
    - id INTEGER PRIMARY KEY AUTO_INCREMENT,
    - nom_media VARCHAR,
    - #produit_id
  );
  
## user (
    - id INTEGER PRIMARY KEY AUTO_INCREMENT,
    - nom VARCHAR,
    - prenom VARCHAR,
    - email VARCHAR,
    - password VARCHAR
    - #genre_id INTEGER,  #Donnant la possibilté de pourvoir, à la page d'acceuil d'un user quelconque, la liste des produit relatif à son genre.
  );
  
## produit (
    - id INTEGER PRIMARY KEY AUTO_INCREMENT,
    - nom VARCHAR,
    - statut VARCHAR,
    - prix INTEGER,
    - #categorie_id INTEGER,
    - #marque_id INTEGER,
    - #couleur_id INTEGER,
    - #taille_id INTEGER,
    - #matiere_id INTEGER,
    - #longueur_id INTEGER
   );
   
## commande (
    - #produit_id INTEGER,
    - #user_id INTEGER,
    - date_de_commande DATE
  );
  
## preference (
    - #produit_id INTEGER,
    - #user_id INTEGER
  );
  
  
  
  
  
