FROM python:3
RUN mkdir /app
WORKDIR /app
RUN pip3 install -r requirements.txt
CMD ["uwsgi","--ini","payment.ini"]