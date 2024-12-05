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


SELECT COUNT(`degrees`.`id`), `departments`.`name`
FROM `departments`
JOIN `degrees`
ON `departments`.`id` = `degrees`.`department_id`
GROUP BY `departments`.`id`, `departments`.`name`

<!-- join -->

# QUERY 5 

<!-- Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia -->

SELECT DISTINCT `students`.`name`, `degrees`.`name`
FROM `students`
JOIN `degrees` ON `degree_id` = `degrees`.`id`
WHERE `degrees`.`name` = 'Corso di Laurea in Economia'

<!-- CON DISTINCT -->

SELECT `students`.`name`, `degrees`.`name`
FROM `students`
JOIN `degrees` ON `degree_id` = `degrees`.`id`
WHERE `degrees`.`name` = 'Corso di Laurea in Economia'

<!-- SENZA DISTINCT -->

# QUERY 6 

<!-- Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di Neuroscienze -->
