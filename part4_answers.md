1. `Find the author with the name 'Kara Melton' and then select all the articles she has written.`

SELECT author_id, title FROM articles WHERE author_id = (SELECT id FROM authors WHERE name = 'Kara Melton');

  --> returned two long titles

2. `Find Ontario in the provinces table and then find all the cities in that province.`

SELECT province_id, city FROM cities WHERE province_id = (SELECT id FROM provinces WHERE name = 'Ontario');

  --> ERROR:  column "city" does not exist

Tried this from another student's submission instead:

  SELECT name FROM cities WHERE province_id = (SELECT id FROM provinces WHERE name = 'Ontario');

    --> returned Toronto and Ottawa

3. `Who wrote the article called 'Coding Bootcamps and Emotional Labor'?`

SELECT author_id FROM authors WHERE author_id = (SELECT id FROM articles WHERE name = 'Coding Bootcamps and Emotional Labor');
  --> ERROR:  column "author_id" does not exist

Trying this instead:
  SELECT name FROM authors WHERE id = (SELECT author_id FROM articles WHERE title = 'Coding Bootcamps and Emotional Labor');
    --> Tilde Ann Thurium

4. `Write a series of SQL queries to find out how many provinces are in Canada.`



5. `How many people live at 4740 McDermott Street?`


6. `What city is 4740 McDermott Street in?`


7. `What province is 4740 McDermott Street in?`


8. `What country is 4740 McDermott Street in?`


9. `Find the person named 'Destini Davis' and then use a series of SQL queries to find what country they live in.`


10. `How many articles has Aditya Mukerjee written?`
