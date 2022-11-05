from python:3.8-alpine
# setup environment variable  
ENV DockerHOME=/home/app/webapp  

# set work directory  
RUN mkdir -p $DockerHOME  

# where your code lives  
WORKDIR $DockerHOME
RUN pip install --upgrade pip 

COPY . $DockerHOME
RUN pip install -r requirements.txt

EXPOSE 8000
CMD python manage.py runserver