FROM ubuntu 
WORKDIR /application 

COPY requirements.txt /application

COPY devops/ /application

RUN apt-get update && \
    apt-get install python3 python3-pip && \
    pip install -r requirement.txt && \
    cd devops

ENTRYPOINT ["python3"]  
CMD ["manage.py","runserver","0.0.0.0:8000"]
