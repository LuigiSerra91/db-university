# query 1
<!-- Contare quanti iscritti ci sono stati ogni anno -->


SELECT COUNT(`id`), `enrolment_date`
FROM `students`
GROUP BY `enrolment_date`


# query 2 

<!-- Contare gli insegnanti che hanno l'ufficio nello stesso edificio -->

SELECT COUNT(`id`) `teachers`, `office_address`
FROM `teachers`
GROUP BY `office_address`

# query 3 

<!-- Calcolare la media dei voti di ogni appello d'esame -->

SELECT AVG(`vote`) AS `avg_vote`, `exam_id`, `student_id`
FROM `exam_student`
GROUP BY `exam_id`, `student_id`


# query 4 

<!-- Contare quanti corsi di laurea ci sono per ogni dipartimento -->


