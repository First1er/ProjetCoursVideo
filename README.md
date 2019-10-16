# ProjetCoursVideo
Ce projet vise à concevoir une sorte de lecteur vidéo en ligne dans le but d'apprendre de manière structurée.

## Rapport de mise en place de la Base de donnée

  #### Nom de la Bd : NanVideoCourses
  Nous avons en tout conçu 9 tables tels que conçu:
  
  Create table Mois (
    id INTEGER PRIMARY KEY AUTO_INCREMENT,
    mois VARCHAR
  );
  
  CREATE TABLE categorieModule (
    id INTEGER PRIMARY KEY AUTO_INCREMENT,
    nom VARCHAR
  );
  
  CREATE TABLE user (
    id INTEGER PRIMARY KEY AUTO_INCREMENT,
    nom VARCHAR,
    prenom VARCHAR,
    email VARCHAR,
    password VARCHAR
  );
  
  CREATE TABLE cours (
    id INTEGER PRIMARY KEY AUTO_INCREMENT,
    titre TEXT,
    description TEXT,
    #module_id INTERGER
  );
  
  CREATE TABLE module (
    id INTEGER PRIMARY KEY AUTO_INCREMENT,
    nom VARCHAR,
    description TEXT,
    duree_module DATE
