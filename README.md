# Multicontainer application

## Dockerizing a React application with Node.js Postgres and NginX - dev and prod - step by step - PART 1 (Dockerizing)


It contains React client, Node.js backend, PostgreSQL and Nginx

### **You can run it in Devlopment mode:** 
```bash
docker-compose up --build 
```

### **Running in Production Mode**
If you want to run the project in Production mode, specify `Dockerfile` in your docker-compose setup.

# Build Docker images Separetly 

## 1. multi-client image (client)
### Image create and run images (create container)
```bash
cd /client
docker build -t abrahimcse/multi-client:01 .
docker run -it -p 4002:3000 abrahimcse/multi-client:01
docker run -d -it -p 4002:3000 abrahimcse/multi-client:01
```
### multi-client image Push
```bash
docker login
docker push abrahimcse/multi-client:01
```
**Image pull from docker hub**
```bash
docker pull abrahimcse/multi-client:01
```

## 2. multi-server image (server)
### Image create and run images (create container) 
```bash 
cd /server
docker build -t abrahimcse/multi-server:01 .
docker run -it -p 4003:5000 abrahimcse/multi-server:01
```
**Image pull from docker hub**
```bash
docker pull abrahimcse/multi-server:01
```

