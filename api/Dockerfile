# reference = https://docs.docker.com/samples/django/
FROM python:3

ENV PYTHONUNBUFFERED=1

WORKDIR /api

COPY requirements.txt /api/

RUN python -m pip install --upgrade pip

RUN pip install -r requirements.txt

COPY . /api/

EXPOSE 8000

CMD ["bash", "-c", "python3 manage.py migrate && python3 manage.py runserver 0.0.0.0:$PORT"]