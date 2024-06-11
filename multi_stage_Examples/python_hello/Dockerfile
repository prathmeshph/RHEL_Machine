FROM python AS builder

WORKDIR /myapp 

COPY . /myapp



FROM python:3.9-slim

WORKDIR /myapp

COPY --from=builder /myapp /myapp

CMD ["python" ,"hello.py"]

