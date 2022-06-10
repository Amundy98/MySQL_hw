# MySQL_hw

 create table if not exists game(
    -> title VARCHAR(30) NOT NULL DEFAULT '',
    -> runtime INT UNSIGNED NOT NULL DEFAULT 0,
    -> genre VARCHAR(20) NOT NULL DEFAULT '',
    -> imdb DECIMAL(7,2) NOT NULL DEFAULT 99999.99,
    -> rating CHAR(8) NOT NULL DEFAULT '',
    -> PRIMARY KEY (title)
    -> );


INSERT INTO game VALUES
    -> ('White Chicks', 20, 'Comedy', 7.8, 'R');
INSERT INTO game VALUES
    -> ('Corpse Bride', 83, 'Fantasy', 8, 'PG');
    INSERT INTO game VALUES
    -> ('Spaceballs', 92, 'Animation', 7.1, 'G'),
    -> ('The Boy', 129, 'Horror', 4.6, 'PG-13');
INSERT INTO game VALUES
    -> ('Gone Girl', 90, 'Thriller', 7.9, 'R');


 INSERT INTO game VALUES
    -> ('Conjuring', 78, 'Horror', 5.8, 'R');


 INSERT INTO game VALUES
    -> ('The Notebook', 110, 'Romance', 4.6, 'PG-13');


 INSERT INTO game VALUES
    -> ('Why did I Get Married', 58, 'Drama/Comedy', 8.9,'PG-13');
    
   INSERT INTO game VALUES
    -> ('Star Wars', 83, 'Sci-Fi', 6, 'PG');
    
   INSERT INTO game VALUES
    -> ('Starship Troopers', 129, 'Sci-Fi', 7.2, 'PG-13');
    
  select title from game where genre = 'Sci-Fi';
    
  select title from game where imdb >= 6.5;
    
  select title from game where rating = 'G' OR rating = 'PG' AND runtime <=100;

  select AVG(imdb) from game;
    
  select MIN(imdb) from game;

  select MAX(imdb) from game;
    
  select AVG(runtime) FROM game WHERE imdb <=7.5;
    
   UPDATE game SET rating = 'R' WHERE title ='Starship Troopers';
     
   select rating, AVG(imdb), MAX(imdb), MIN(imdb) FROM game GROUP BY rating HAVING COUNT(*)>1;
     
   DELETE FROM game WHERE rating ='R';

    
    
    
  
