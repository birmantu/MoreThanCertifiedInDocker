FROM python:alpine

RUN apk update
RUN apk upgrade
RUN apk add curl

WORKDIR /app
COPY ./requirements.txt /app/requirements.txt 
RUN pip install -r requirements.txt
COPY ./app.py /app/app.py

ENV DEVICE="device#1"
EXPOSE 5000
HEALTHCHECK --interval=5s --timeout=5s CMD curl -f http://localhost:5000 || exit 1

ENTRYPOINT [ "python" ]
CMD [ "app.py", "--host", "0.0.0.0" ]