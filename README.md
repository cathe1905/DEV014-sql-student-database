# Student Database

## Tutorial 1
TERMINAL BASH 
```
1 echo hello SQL
2 psql --username-freecodecamp --dbname-postgres
3 psql --help
4 psql --catherin-freecodecamp --dbstudents-postgres
5 psql --username=freecodecamp --dbname-postgres
6 psql --username=freecodecamp --dbname=postgres
7 \c students
8 psql --username=freecodecamp --dbname=students
9 psql --username=freecodecamp --dbname=students
10 touch insert_data.sh
11 chmod +x insert_data.sh
12 ./insert_data.sh
13 ./insert_data.sh
14 declare -p IFS
15 ./insert_data.sh
16 ./insert_data.sh
17 ./insert_data.sh
18 ./insert_data.sh
19 cp courses.csv courses_test.csv
20 ./insert_data.sh
21 psql --username=freecodecamp --dbname=students
22 TRUNCATE majors, students, majors_courses;
23 ./insert_data.sh
24 ./insert_data.sh
25 ./insert_data.sh
26 psql --username=freecodecamp --dbname=students
27 ./insert_data.sh
28 ./insert_data.sh
29 ./insert_data.sh
30 cp students.csv students_test.csv
31 ./insert_data.sh
32 ./insert_data.sh
33 ./insert_data.sh
34 ./insert_data.sh
35 ./insert_data.sh
36 ls
37 rm students_test.csv
38 rm courses_test.csv
39 ls
40 ls
41 pg_dump --help
```  
   
TERMINAL PSQL
``` 
  TRUNCATE majors;  
  TRUNCATE majors, students, majors_courses;  
  ./insert_data.sh  
  SELECT * FROM courses;  
  SELECT * FROM courses;  
  SELECT * FROM majors;  
  SELECT * FROM courses;  
  SELECT * FROM majors_courses;  
  \d students  
  SELECT * FROM students;  
  SELECT * FROM students;  
  SELECT * FROM majors;  
  SELECT * FROM courses;  
  SELECT * FROM majors_courses;  
  ls  
  history  
  \c  
  \s  
  \q  
``` 
  ##Tutorial 2  
  
  TERMINAL BASH  
``` 
1  echo hello SQL  
2  psql -U postgres < students.sql  
3  touch student_info.sh  
4  chmod +x student_info.sh  
5  ./student_info.sh  
6  ./student_info.sh  
7  ./student_info.sh  
8  ./student_info.sh  
9  history  
10 psql -U postgres < students.sql
11 touch student_info.sh
12 chmod +x student_info.sh
13 ./student_info.sh
14 ./student_info.sh
15 ./student_info.sh
16 ./student_info.sh
17 history
19 psql --username=freecodecamp --dbname=postgres
20 history
21 cat ~/.psql_history
22 ./student_info.sh
23 ./student_info.sh
24 ./student_info.sh
25 psql --username=freecodecamp --dbname=postgres
26 cat ~/.psql_history
27 history
28 \c students
29 ./student_info.sh
30 ./student_info.sh
31 ./student_info.sh
32 ./student_info.sh
33 ./student_info.sh
34 history
```
TERMINAL PSQL  
```
\c students  
SELECT * FROM courses;  
SELECT * FROM courses WHERE course LIKE '_lgorithms';  
SELECT * FROM courses WHERE course LIKE '%lgorithms';  
SELECT * FROM courses WHERE course LIKE 'Web%';  
SELECT * FROM courses WHERE course LIKE '_e';  
SELECT * FROM courses WHERE course LIKE '_e%';  
SELECT * FROM courses WHERE course LIKE '% %';  
SELECT * FROM courses WHERE course NOT LIKE '% %';  
SELECT * FROM courses WHERE course LIKE '%A%';  
SELECT * FROM courses WHERE course ILIKE '%A%';  
SELECT * FROM courses WHERE course NOT ILIKE '%A%';  
SELECT * FROM courses WHERE course NOT ILIKE '%A%' AND NOT LIKE '% %';  
SELECT * FROM courses WHERE course NOT ILIKE '%A%' AND LIKE '% %';  
SELECT * FROM courses WHERE course NOT ILIKE '%A%' AND ILIKE '% %';  
SELECT * FROM courses WHERE course NOT ILIKE '%A%' AND course LIKE '% %';  
SELECT * FROM students;  
SELECT * FROM students WHERE major_id IS NULL;  
SELECT * FROM students WHERE gpa IS NULL;  
SELECT * FROM students WHERE gpa IS NOT NULL;  
SELECT * FROM students WHERE major_id IS NULL;  
SELECT * FROM students WHERE major_id IS NULL AND gpa IS NOT NULL;  
SELECT * FROM students WHERE major_id IS NULL AND gpa IS NULL;  
SELECT * FROM students ORDER BY gpa;  
SELECT * FROM students ORDER BY gpa DESC;  
SELECT * FROM students ORDER BY gpa DESC, first_name;  
SELECT * FROM students ORDER BY gpa DESC, first_name LIMIT 10;  
SELECT * FROM students WHERE gpa IS NOT NULL ORDER BY gpa DESC, first_name LIMIT 10;  
SELECT * FROM courses;  
SELECT MIN(gpa) FROM students;  
SELECT MAX(gpa) FROM students;  
\q  
_HiStOrY_V2_  
\c students  
SELECT SUM(major_id) FROM students;  
SELECT AVG(major_id) FROM students;  
SELECT CEIL(AVG(major_id)) FROM students;  
SELECT ROUND(AVG(major_id)) FROM students;  
SELECT ROUND(AVG(major_id,5)) FROM students;  
SELECT ROUND(AVG(major_id), 5) FROM students;  
SELECT COUNT(*) FROM majors;  
SELECT COUNT(*) FROM students;  
SELECT COUNT(major_id) FROM students;  
SELECT DISTINCT COUNT(major_id) FROM students;  
SELECT DISTINCT (major_id) FROM students;  
SELECT major_id FROM students GROUP BY major_id;  
SELECT * FROM students GROUP BY major_id;  
SELECT * FROM students;  
SELECT COUNT(student_id) FROM students ORDER BY major_id;  
SELECT COUNT(*) FROM students ORDER BY major_id;  
SELECT major_id, COUNT(*) FROM students ORDER BY major_id;  
SELECT major_id, COUNT(*) FROM students GROUP BY major_id;  
SELECT major_id, COUNT(*), MIN(gpa) FROM students GROUP BY major_id;  
SELECT major_id, MIN(gpa) FROM students GROUP BY major_id;  
SELECT major_id, MIN(gpa), MAX(gpa) FROM students GROUP BY major_id;  
SELECT major_id, MIN(gpa), MAX(gpa) FROM students GROUP BY major_id HAVING MAX(gpa) = 4.0;  
SELECT major_id, MIN(gpa) AS min_gpa, MAX(gpa) FROM students GROUP BY major_id HAVING MAX(gpa) = 4.0;  
SELECT major_id, MIN(gpa) AS min_gpa, MAX(gpa) AS max_gpa FROM students GROUP BY major_id HAVING MAX(gpa) = 4.0;  
SELECT major_id AS number_of_students, MIN(gpa) AS min_gpa, MAX(gpa) AS max_gpa FROM students GROUP BY major_id HAVING MAX(gpa) = 4.0;  
SELECT major_id, COUNT(*) AS number_of_students FROM students GROUP BY major_id;  
SELECT major_id, COUNT(*) AS number_of_students FROM students GROUP BY major_id HAVING number_of_students < 8;  
SELECT major_id, COUNT(*) AS number_of_students FROM students GROUP BY major_id HAVING COUNT(*) < 8;  
SELECT major_id, COUNT(*) AS number_of_students, ROUND(AVG(gpa), 2) AS average_gpa FROM students GROUP BY major_id HAVING COUNT(*) > 1;  
SELECT * FROM majors FULL JOIN students ON majors.major_id = students.major_id;  
SELECT * FROM students FULL JOIN majors ON students.major_id = majors.major_id;  
SELECT * FROM students LEFT JOIN majors ON students.major_id = majors.major_id;  
SELECT * FROM students RIGHT JOIN majors ON students.major_id = majors.major_id;  
SELECT * FROM students INNER JOIN majors ON students.major_id = majors.major_id;  
SELECT * FROM students LEFT JOIN majors ON students.major_id = majors.major_id;  
SELECT * FROM majors LEFT JOIN students ON majors.major_id = students.major_id;  
SELECT * FROM majors INNER JOIN students ON majors.major_id = students.major_id;  
SELECT * FROM students RIGHT JOIN majors ON students.major_id = majors.major_id;  
SELECT * FROM majors RIGHT JOIN students ON majors.major_id = students.major_id;  
SELECT * FROM majors FULL JOIN students ON majors.major_id = students.major_id;  
SELECT * FROM majors LEFT JOIN students ON majors.major_id = students.major_id;  
SELECT * FROM majors INNER JOIN students ON majors.major_id = students.major_id;  
SELECT major FROM majors INNER JOIN students ON majors.major_id = students.major_id;  
SELECT DISTINCT(major) FROM majors INNER JOIN students ON majors.major_id = students.major_id;  
SELECT * FROM majors FULL JOIN students ON majors.major_id = students.major_id;  
SELECT * FROM majors RIGHT JOIN students ON majors.major_id = students.major_id;  
SELECT * FROM students RIGHT JOIN majors ON students.major_id = major.major_id;  
SELECT * FROM students RIGHT JOIN majors ON students.major_id = majors.major_id;  
SELECT majors.major FROM students RIGHT JOIN majors ON students.major_id = majors.major_id WHERE students.first_name IS NULL;  
SELECT majors.major FROM students RIGHT JOIN majors ON students.major_id = majors.major_id WHERE students.student_id IS NULL;  
SELECT * FROM students RIGHT JOIN majors ON students.major_id = majors.major_id WHERE student_id IS NULL;  
SELECT * FROM students RIGHT JOIN majors ON students.major_id = majors.major_id WHERE student_id IS NULL;  
SELECT major FROM students RIGHT JOIN majors ON students.major_id = majors.major_id WHERE student_id IS NULL;  
SELECT * FROM students INNER JOIN majors ON students.major_id = majors.major_id;  
SELECT * FROM students RIGHT JOIN majors ON students.major_id = majors.major_id;  
SELECT * FROM students LEFT JOIN majors ON students.major_id = majors.major_id;  
SELECT * FROM students LEFT JOIN majors ON students.major_id = majors.major_id WHERE major = 'Data Science';  
SELECT * FROM students LEFT JOIN majors ON students.major_id = majors.major_id WHERE major = 'Data Science' AND gpa >= 3.8;  
SELECT * FROM students LEFT JOIN majors ON students.major_id = majors.major_id WHERE major = 'Data Science' OR gpa >= 3.8;  
SELECT first_name, last_name, major_id, gpa FROM students LEFT JOIN majors ON students.major_id = majors.major_id WHERE major = 'Data Science' OR gpa >= 3.8;  
SELECT first_name, last_name, majors.major_id, majors.gpa FROM students LEFT JOIN majors ON students.major_id = majors.major_id WHERE major = 'Data Science' OR gpa >= 3.8;  
SELECT first_name, last_name, majors.major, majors.gpa FROM students LEFT JOIN majors ON students.major_id = majors.major_id WHERE major = 'Data Science' OR gpa >= 3.8;  
SELECT first_name, last_name, major, gpa FROM students LEFT JOIN majors ON students.major_id = majors.major_id WHERE major = 'Data Science' OR gpa >= 3.8;  
SELECT * FROM students INNER JOIN majors ON students.major_id = majors.major_id;  
SELECT * FROM students FULL JOIN majors ON students.major_id = majors.major_id;  
SELECT * FROM students FULL JOIN majors ON students.major_id = majors.major_id WHERE first_name LIKE '%ri%' OR major LIKE '%ri%';  
SELECT first_name, major FROM students FULL JOIN majors ON students.major_id = majors.major_id WHERE first_name LIKE '%ri%' OR major LIKE '%ri%';  
SELECT major FROM students RIGHT JOIN majors ON students.major_id = majors.major_id WHERE student_id IS NULL OR first_name LIKE '%ma%' ORDER BY major;  
SELECT * FROM students RIGHT JOIN majors ON students.major_id = majors.major_id WHERE student_id IS NULL OR first_name LIKE '%ma%' ORDER BY major;  
SELECT major FROM students FULL JOIN majors ON students.major_id = majors.major_id WHERE student_id IS NULL OR first_name LIKE '%ma%' ORDER BY major;  
SELECT major FROM students FULL JOIN majors ON students.major_id = majors.major_id WHERE student_id IS NULL OR first_name LIKE '%ma%' ORDER BY major;  
\c students  
SELECT * FROM students FULL JOIN majors ON students.major_id = majors.major_id;  
SELECT students.major_id FROM students FULL JOIN majors ON students.major_id = majors.major_id;  
SELECT students.major_id FROM students FULL JOIN majors AS m ON students.major_id = majors.major_id;  
SELECT students.major_id FROM students FULL JOIN majors AS 'm' ON students.major_id = majors.major_id;  
SELECT students.major_id FROM students FULL JOIN majors AS "m" ON students.major_id = majors.major_id;  
SELECT students.major_id FROM students FULL JOIN majors AS m ON students.major_id = .major_id;  
SELECT students.major_id FROM students FULL JOIN majors AS m ON students.major_id = m.major_id;  
SELECT students.major_id FROM students AS s FULL JOIN majors AS m ON s.major_id = m.major_id;  
SELECT s.major_id FROM students AS s FULL JOIN majors AS m ON s.major_id = m.major_id;  
SELECT * FROM students FULL JOIN majors USING(major_id);  
SELECT * FROM majors_courses;  
SELECT * FROM students FULL JOIN majors USING(major_id) FULL JOIN majors_courses USING(major_id);  
SELECT * FROM courses;  
SELECT * FROM students FULL JOIN majors USING(major_id) FULL JOIN majors_courses USING(major_id) FULL JOIN courses USING(course_id);  
SELECT * FROM students;  
SELECT DISTINCT(course) FROM students FULL JOIN majors USING(major_id) FULL JOIN majors_courses USING(major_id) FULL JOIN courses USING(course_id) WHERE student_id IS NULL OR first_name = 'Obie' ORDER BY course DESC;  
SELECT * FROM students RIGHT JOIN majors USING(major_id) INNER JOIN majors_courses USING(major_id) INNER JOIN courses USING(course_id);  
SELECT course FROM students RIGHT JOIN majors USING(major_id) INNER JOIN majors_courses USING(major_id) INNER JOIN courses USING(course_id) GROUP BY course HAVING COUNT(course) = 1 ORDER BY course;  
SELECT course FROM students RIGHT JOIN majors USING(major_id) INNER JOIN majors_courses USING(major_id) INNER JOIN courses USING(course_id) WHERE student_id IS NOT NULL GROUP BY course HAVING COUNT(course) = 1 ORDER BY course;  

```

  

