# query 1
<!-- Contare quanti iscritti ci sono stati ogni anno -->


SELECT COUNT(`id`), `enrolment_date`
FROM `students`
GROUP BY `enrolment_date`


# query 2 

<!-- Contare gli insegnanti che hanno l'ufficio nello stesso edificio -->

