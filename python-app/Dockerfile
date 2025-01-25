FROM ubuntu // creates a new build from base image
WORKDIR /application  //Creating a folder to stored / place you files 

COPY requirements.txt /application //copying requirements.txt file to /application folder

COPY devops/ /application //copying devops folder to application folder

RUN apt-get update && \
    apt-get install python3 python3-pip && \
    pip install -r requirement.txt && \
    cd devops \\ installing packages and requirement.txt file and cd to devops

ENTRYPOINT ["python3"]  \\this caannot be changed
CMD ["manage.py","runserver","0.0.0.0:8000"] \\executing \ running manage.py on 8000 server
