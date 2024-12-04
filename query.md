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

# QUERY 9 

INSERT INTO students (degree_id, name, surname, date_of_birth, fiscal_code, enrolment_date, registration_number, email)
VALUES (2, 'Mario', 'Rossi', '1990-01-01', 'RSSMRA90A01H501Z', '2024-12-04', '987654', 'mario.rossi@example.com');

# QUERY10

UPDATE teachers SET office_number=126 WHERE id=58



