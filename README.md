# ProjetCoursVideo
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
    
