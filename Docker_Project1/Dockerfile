# Dockerfile, Image, Container
FROM python:3.8
# provides us python from dockerhub

ADD main.py . 

RUN pip install requests beautifulsoup4
# runs pip install for beautiful soup lib

# runs python main.py in container terminal
CMD [ "python", "./main.py" ]
 
