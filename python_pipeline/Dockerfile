FROM python:alpine3.17

WORKDIR /usr/app/src

EXPOSE 5000

#RUN mkdir ./templates
#RUN mkdir ./static

#COPY ./templates/ ./templates
#COPY ./static ./static

COPY requirements.txt ./

RUN pip install --no-cache-dir -r requirements.txt

COPY ["app.py", "./"]

#CMD [ "flask", "run","--host","0.0.0.0"]
