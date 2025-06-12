# 1. Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia

```SQL

SELECT
`students`.`id` AS "id_student",
`students`.`name` AS "name_student",
`students`.`surname` AS "surname_student",
`degrees`.`id` AS "id_degree",
`degrees`.`name` AS "name_degree"
FROM `degrees`
INNER JOIN `students`
ON `degrees`.`id`= `students`.`degree_id`
WHERE `degrees`.`name`="Corso di Laurea in Economia"
;

```

2. Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di Neuroscienze

```SQL

SELECT
`degrees`.`id` AS "degree_id",
`degrees`.`level` AS "degree_level",
`courses`.`id` AS "course_id",
`courses`.`name` AS "course_name",
`departments`.`id` AS "department_id",
`departments`.`name` AS "department_name"
FROM `degrees`
INNER JOIN `departments`
ON `departments`.`id`= `degrees`.`department_id`
INNER JOIN `courses`
ON `degrees`.`id`= `courses`.`degree_id`
WHERE `departments`.`name` = "Dipartimento di Neuroscienze" AND `degrees`.`level` = "magistrale"
;

```

3. Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44)

```SQL

```

4. Selezionare tutti gli studenti con i dati relativi al corso di laurea a cui sono iscritti e il relativo dipartimento, in ordine alfabetico per cognome e nome

```SQL

```

5. Selezionare tutti i corsi di laurea con i relativi corsi e insegnanti

```SQL

```

6. Selezionare tutti i docenti che insegnano nel Dipartimento di
   Matematica (54)

```SQL

```

7. BONUS: Selezionare per ogni studente il numero di tentativi sostenuti per ogni esame, stampando anche il voto massimo. Successivamente, filtrare i tentativi con voto minimo 18

```SQL

```
