# QUERY1

SELECT `date_of_birth`
FROM `students`
WHERE YEAR (`date_of_birth`) = 1990


# QUERY2

SELECT `cfu`
FROM `courses`
WHERE `cfu` > 10;

# QUERY 3

SELECT `date_of_birth`
FROM `students`
WHERE YEAR(`date_of_birth`) < 1994;

# QUERY 4

SELECT *
FROM `courses`
WHERE YEAR = 1
AND period = 'I semestre';

# QUERY 5

SELECT *
FROM `exams`
WHERE hour >'14:00'
AND date = '2020-06-20';

# QUERY 6 

SELECT *
FROM `degrees`
WHERE level = 'magistrale';

# QUERY 7 

SELECT COUNT('id')
FROM `departments`

# QUERY 8 


SELECT COUNT(*)
FROM `teachers`
WHERE PHONE is null;


