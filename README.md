# ESERCIZIO BASE
1. SELECT `name`,`surname`,`date_of_birth` FROM `students` WHERE YEAR(`date_of_birth`)=1990; 
2. SELECT `name`,`cfu` FROM `courses` WHERE `cfu` > 10; 
3. SELECT `name`,`surname`,`date_of_birth` FROM `students` WHERE DATE_SUB(CURDATE(), INTERVAL 30 YEAR) > `date_of_birth`;
4. SELECT `name`, `period`, `year` FROM `courses` WHERE `year` = 1 AND `period` = 'I semestre'; 
5. SELECT `course_id`, `date`, `hour` FROM `exams` WHERE `date` = '2020-06-20' AND CAST(`hour` AS TIME) > '14:00'; 
6. SELECT `level` FROM `degrees` WHERE `level` = 'magistrale'; 
7. SELECT COUNT(id) AS 'numero_dipendenti' FROM `departments`; 
8. SELECT `name`,`phone` FROM `teachers` WHERE `phone` IS NULL; 

# BONUS
1. SELECT COUNT(ID) AS `number_of_students`, LEFT(`enrolment_date`, 4) AS `enrolment_year` FROM `students` GROUP BY `enrolment_year`; 
2. SELECT COUNT(`office_address`) AS `office_counter`,`office_address` FROM `teachers` GROUP BY `office_address`; 
3. SELECT `exam_id`,CEILING(AVG(`vote`)) AS 'media_dei_voti' FROM `exam_student` GROUP BY `exam_id`; 
4. SELECT COUNT(ID) AS `degrees_count`,`department_id` FROM `degrees` GROUP BY `department_id`; 