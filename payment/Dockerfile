FROM python:3-alpine

RUN mkdir /app
COPY . /app
WORKDIR /app

RUN pip install -r requirements.txt
ENV FLASK_APP app.py

CMD ["flask", "run", "--host", "0.0.0.0", "--port", "5002", "--with-threads"]
