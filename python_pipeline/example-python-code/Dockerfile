FROM python:alpine3.17

WORKDIR /usr/app/src

EXPOSE 5000

COPY requirements.txt ./

RUN pip install --no-cache-dir -r requirements.txt

COPY ["app.py", "./"]

CMD [ "flask", "run","--host","0.0.0.0"]
