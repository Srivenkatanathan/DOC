FROM ubuntu 
WORKDIR /application 

COPY requirements.txt /application

COPY devops/ /application

RUN apt-get update && \
    apt-get install python3 python3-pip && \
    pip install -r requirement.txt && \
    cd devops

SHELL ["/bin/bash", "-c"]

RUN python3 -m venv venv1 && \
source venv1/bin/activate && \
pip install --no-cache-dir -r requirements.txt

EXPOSE 8000

CMD source venv1/bin/activate && python3 manage.py runserver 0.0.0.0:8000
