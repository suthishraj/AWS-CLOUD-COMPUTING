DOCKER PYTHON FLASK APPLICATION

FROM python:3.9-slim

WORKDIR /app

COPY requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt

COPY . .

EXPOSE 8080

CMD ["python", "app.py"]

DOCKER IMAGE 
"A Docker image is a read-only template that contains everything needed to run an application, including the application code, runtime, libraries, dependencies, and configuration files. It is used to create Docker containers."

Simple Definition

"A Docker image is like a blueprint or template used to create Docker containers."

Real-Life Example
Docker Image = Cake recipe 🍰
Docker Container = Cake made from that recipe

You can bake many cakes from the same recipe, just as you can create many containers from the same Docker image.

docker build -t image-name .
