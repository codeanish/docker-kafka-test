FROM python:3.9-slim-buster

RUN pip install pipenv

COPY Pipfile /usr/src/Pipfile
WORKDIR /usr/src

RUN pipenv lock --requirements > requirements.txt
RUN pip install -r requirements.txt

COPY consumer.py /usr/src/consumer.py

CMD ["python", "-u", "consumer.py"]