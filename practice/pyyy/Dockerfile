FROM ubuntu

RUN apt-get update && apt-get install -y pip

WORKDIR /myapp

COPY . .

CMD ["python" ,"app.py"]
