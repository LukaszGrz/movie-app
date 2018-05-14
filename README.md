# movie-app

Simple Java Rest Api application using Spring Boot, MongoDB and docker-compose


How to start the application:

- download project from GitHub
- using Power Shell (or other bash/CMD/Docker) go to directory where "Dockerfile" is allocated
- first build project by typing- " docker build -t movie . " 
- then build application by- " docker-compose up "

Application will start on localhost:8088


By using endpoints you are able to :

1./ view list of all movies sorted by ranting
localhost:8088/movies/all/

2./ add new movie to the DB
localhost:8088/movies
body needed, below example jason:

    {
        "title": "TestMovie",
        "ratings": 1.0,
        "director": "testDirector",
        "actors": "TestActors"
    }
    
3./ delete movie by ID
localhost:8088/movies/id_movie

4./ add review to movie
localhost:8088/reviews/id_movie/addReview
body needed, below example jason:

    {
        "description": "Best film...."
    }

5./ show All reviews to accept
localhost:8088/reviews/all/toReview

6./ accept review for movie
localhost:8088/reviews/id_movie/accept/id_review
