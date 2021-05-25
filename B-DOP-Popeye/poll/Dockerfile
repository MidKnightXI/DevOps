FROM python:3
WORKDIR /pyflask
COPY . .
RUN [ "pip3", "install", "--no-cache-dir", "-r", "requirements.txt" ]
EXPOSE 80
CMD [ "flask", "run", "--host=0.0.0.0", "--port=80" ]