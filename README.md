# CS50SQL_ex2
SQL query exercises

1. 
SELECT birth FROM people WHERE name='Jerry Seinfeld';
1954

2.
SELECT COUNT(*) FROM ratings WHERE rating = 10;
27

3.
SELECT genre FROM genres WHERE show_id =
   (SELECT id FROM shows WHERE title='The Crown');
drama, history

4.
SELECT name FROM people WHERE id=
   (SELECT person_id FROM writers WHERE show_id=
      (SELECT id FROM shows WHERE title='Arrested Development'));
Mitchell Hurwitz

5.
SELECT title FROM shows WHERE id=
   (SELECT show_id FROM stars WHERE person_id=
      (SELECT id FROM people WHERE name='Allison Janney'));
Morton & Hayes
