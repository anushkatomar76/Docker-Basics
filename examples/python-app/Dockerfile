#Collect the Base Image
FROM ubuntu

#Set the Workdir
WORKDIR /app

#copy all the code from src to des
COPY requirements.txt /app

COPY devops /app

#update all the dependencies

RUN apt-get update && \
    apt-get install -y python3 python3-pip && \
    pip install -r requirements.txt \
    cd devops

ENTRYPOINT ["python3"]
CMD ["manage.py","runserver","0.0.0.0:8000"]
 
