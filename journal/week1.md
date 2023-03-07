# Week 1 — App Containerization
In week1 I learnt how to make docker image, container and docker compose. Also not to forget to commit our code in our repository.
In spending consideration, learnt comparison between GitPod, GitHub and AWS Cloud9 pricing.

# Containerize Application (Dockerfiles, Docker Compose)	
## Make Sure Flask Backend is Working

```
export FRONTEND_URL="*"
export BACKEND_URL="*"
python3 -m flask run --host=0.0.0.0 --port=4567
```

then we expose it public, and open this path `/api/activities/home`, if it right and got json

## Make Dockerfile
Created Dockerfile in `backend-flask/Dockerfile`

```
FROM python:3.10-slim-buster

WORKDIR /backend-flask

COPY requirements.txt requirements.txt
RUN pip3 install -r requirements.txt

COPY . .

ENV FLASK_ENV=development

EXPOSE ${PORT}
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]
```
### Build Backend Docker Image
docker build -t  backend-flask .

### Run Backend Docker Image
docker run --rm -p 4567:4567 -it -e FRONTEND_URL='*' -e BACKEND_URL='*' backend-flask
