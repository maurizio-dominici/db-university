# ESERCIZIO (SELECT)

1. Selezionare tutti gli studenti nati nel 1990 (160)

```SQL

SELECT
`date_of_birth`
FROM `students`
WHERE `date_of_birth` BETWEEN "1990-01-01" AND "1990-12-31"
;

```

2. Selezionare tutti i corsi che valgono più di 10 crediti (479)

```SQL

SELECT `cfu`
FROM `courses`
WHERE `cfu` > "10"
;

```

3. Selezionare tutti gli studenti che hanno più di 30 anni

```SQL

SELECT `date_of_birth`
FROM `students`
WHERE `date_of_birth` > "1995-06-11"
;

```

4. Selezionare tutti i corsi del primo semestre del primo anno di
   un qualsiasi corso di laurea (286)

```SQL

SELECT
COUNT(*)
FROM courses
WHERE `period` = "I semestre" AND
`year` = "1"
;


```

5. Selezionare tutti gli appelli d'esame che avvengono nel pomeriggio (dopo le 14) del 20/06/2020 (21)

```SQL

SELECT
COUNT(*)
FROM `exams`
WHERE `date` = "2020-06-20" AND `hour` > "14:00"
;

```

6. Selezionare tutti i corsi di laurea magistrale (38)

```SQL

SELECT
COUNT(`level`)
FROM `degrees`
WHERE `level` = "magistrale"
;

```

7. Da quanti dipartimenti è composta l'università? (12)

```SQL
SELECT
COUNT(`id`)
FROM `departments`
;

```

8. Quanti sono gli insegnanti che non hanno un numero di telefono? (50)

```SQL

SELECT
COUNT(*)
FROM `teachers`
where `phone` IS NULL
;

```

---

# BONUS (GROUP BY)

1. Contare quanti iscritti ci sono stati ogni anno

```SQL

SELECT
YEAR(`enrolment_date`) ,
COUNT(*)
FROM
`students`
GROUP BY
YEAR(`enrolment_date`)
;

```

2. Contare gli insegnanti che hanno l'ufficio nello stesso edificio

```SQL
SELECT `office_address`,
COUNT(*)
FROM `teachers`
GROUP BY `office_address`
ORDER BY `office_address` ASC
;


```

3. Calcolare la media dei voti di ogni appello d'esame

```SQL

SELECT
AVG(`vote`)
FROM `exam_student`
GROUP BY
(`vote`)
;

```

4. Contare quanti corsi di laurea ci sono per ogni dipartimento
