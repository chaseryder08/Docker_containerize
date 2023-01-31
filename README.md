# DOCKER - Containerize Python applications
---
> This project uses docker to containerize a IMDB move scraper application

## STEPS:
1) Create main.py python script - this scrapes IMDB and suggests a movie from their website
*  Imported libraries:
    
    * random, requests (HTML Parser), 
    * requests - allows you to send HTTP requests using Python. 
    * Beautiful soup - package to parse html/xml to extract data

![alt text](Docker1.PNG)
2) Create docker image: 

- specify base image FROM 
- ADD python file
- install dependencies - RUN
- CMD to run python main.py in docker terminal*

3) Creates docker image:
-  docker build -t dockerfun .
- pulls python image, adds main.py, then install modules

![alt text](Docker2.PNG)
4) Start container 
   - docker run -t -i dockerfun
    * (-i = gives sudo terminal / -i - puts in interactive mode since there is user input requested)

---

# Project 2: FAST-API 
1) Create new dir
2) create virtual environment
3) install dependencies
   - pip install fastapi
   - pip install uvicorn (web server)
1) run python script
2) web browser shows server is running

## DOCKERIZE APPLICATION
6) pip freeze > requirements.txt
> writes all dependencies into file
7) Create docker file in root folder
8) Create docker container with all dependencies
> docker build -t python-fastapi . 
>
> Issue is it doesn't work --
 * when run container need to map port :
 * docker run -p 8000:8000 python-fastapi (Map port 8000:8000)
 * put in arguments in uvicorn.run(app, port=8000, host="0.0.0.0")
 * Need to specify host address and port

![alt text](docker_web.PNG)

9) rebuild image :
> docker build -t python-fastapi .
> docker run -p 8000:8000 python-fastapi 
![docker](dockerps2.PNG)
10) Check docker hub can see container
11) In terminal, 'docker ps' shows running docker containers
12) Can access docker container terminal in docker hub or in terminal --
