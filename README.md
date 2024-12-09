# Multicontainer application

## Dockerizing a React application with Node.js Postgres and NginX - dev and prod - step by step - PART 1 (Dockerizing)


It contains React client, Node.js backend, PostgreSQL and Nginx

### **You can run it in Production mode:** 
```bash
docker-compose up --build 
```

### **Running in Development Mode**
If you want to run the project in development mode, specify `Dockerfile.dev` in your docker-compose setup. Then, use the following command:
```bash
docker-compose -f docker-compose.dev.yml up --build
```