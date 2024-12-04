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
