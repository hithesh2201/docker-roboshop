FROM python:3.9.18-alpine-3.19
EXPOSE 8080
USER root
WORKDIR /app
COPY requirements.txt /app/
RUN apk add python3-dev build-base linux-headers pcre-dev
RUN pip install -r requirements.txt
COPY *.py /app/
COPY payment.ini /app/
ENV AMQP_USER=roboshop \
    AMQP_PASS=roboshop123
#CMD ["python", "payment.py"]
CMD ["uwsgi", "--ini", "payment.ini"]