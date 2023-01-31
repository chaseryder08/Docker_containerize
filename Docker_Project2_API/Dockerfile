FROM python:3.8

# want to organize files in folder and go into folder
WORKDIR /fastapi-app

# copy requirements into working directory
COPY requirements.txt .

#install dependencies
RUN pip install -r requirements.txt

#copy whole app folder with main.py file
COPY ./app ./app

CMD ["python", "./app/main.py"]

