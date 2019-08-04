FROM python:3.5
MAINTAINER Devansh_Anhal
ADD . /usr/src/app
WORKDIR /usr/src/app
COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt
EXPOSE 8000
CMD exec gunicorn Elearning:application --b 0.0.0.0:8000 --workers 3
gunicorn --log-file=- Elearning:application