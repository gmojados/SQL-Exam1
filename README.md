# SQL-Exam1
1.) mysql> INSERT INTO movies (Title, Runtime, Genre, IMDB_Score, Rating) 
    -> VALUES ("Dune", 130, "Sci-Fi", 8.4, "R"), 
    ->        ("Iron Man", 120, "Action", 9.0, "PG-13");

2.) mysql> Select * from movies
    -> where genre = 'Sci-fi';

3.)mysql> Select * from movies
    -> where imdb_score > 6.5;

4.) mysql> Select* from movies
    -> where (rating = 'G' OR rating = 'PG') and runtime <100;

5.) mysql> select genre, avg(runtime) as avg_runtime
    -> from movies
    -> where imdb_score <7.5
    -> group by genre;
    
6.) mysql> update movies
    -> Set Rating = 'R'
    -> Where title = "Starship Troopers";
    
7.)

8.) mysql> select avg(imdb_score), max(imdb_score), min(imdb_score)
    -> from movies;

    
9.) mysql> SELECT Rating, 
    ->        AVG(IMDB_Score) AS AVG_IMDB_Score, 
    ->        MAX(IMDB_Score) AS MAX_IMDB_Score, 
    ->        MIN(IMDB_Score) AS MIN_IMDB_Score
    -> FROM movies
    -> GROUP BY Rating
    -> HAVING COUNT(*) > 1;
