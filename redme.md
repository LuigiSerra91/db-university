Modellare la struttura di un database per memorizzare tutti i dati riguardanti una università:
sono presenti diversi Dipartimenti (es.: Lettere e Filosofia, Matematica, Ingegneria ecc.);
ogni Dipartimento offre più Corsi di Laurea (es.: Civiltà e Letterature Classiche, Informatica, Ingegneria Elettronica ecc..)
ogni Corso di Laurea prevede diversi Corsi (es.: Letteratura Latina, Sistemi Operativi 1, Analisi Matematica 2 ecc.);
ogni Corso può essere tenuto da diversi Insegnanti;
ogni Corso prevede più appelli d'Esame;
ogni Studente è iscritto ad un solo Corso di Laurea;
ogni Studente può iscriversi a più appelli di Esame;
per ogni appello d'Esame a cui lo Studente ha partecipato, è necessario memorizzare il voto ottenuto, anche se non sufficiente. Pensiamo a quali entità (tabelle) creare per il nostro database e cerchiamo poi di stabilirne le relazioni. Infine, andiamo a definire le colonne e i tipi di dato di ogni tabella.

 ## structure university

 - dipartimenti 
 - corsi laurea 
 - insegnanti 
 - esami(appelli d'esame)
 - studenti 
 - partecipazioni agli esami

 --------------------------------------------------

 ## dipartimenti 
- id_dipartimento (PK)| INT | NOT NULL
- nome | VARCHAR(250) NOTNULL

## corsi laurea 
- id_corso_laurea | INT PK
- nome | VARCHAR(250) NOTNULL
- id_dipartimento | INT 

## corsi
- id_corso | INT PK
- nome | VARCHAR(250) NOTNULL
- id_corso_laurea | INT,
- drescrizione | TEXT()

## insegnanti 
- id_insegnante | INT PRIMARY KEY,
- nome VARCHAR(250) | NOT NULL,
- cognome VARCHAR(255) | NOT NULL,
- email | VARCHAR(250) 


## esami 
 -  id_esame INT PRIMARY KEY,
 - id_corso INT,
 - data DATE,
 - sessione VARCHAR(255),


## studenti 
 - id_studente INT PRIMARY KEY,
 - nome VARCHAR(255) NOT NULL,
 - cognome VARCHAR(255) NOT NULL,
 - data_nascita DATE,
 - id_corso_laurea INT,


## partecipazione esame
 - id_studente INT,
 - id_esame INT,
 - voto DECIMAL(5,2),
 - esito VARCHAR(50),



