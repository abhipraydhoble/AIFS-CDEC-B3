<img width="951" height="218" alt="image" src="https://github.com/user-attachments/assets/7e9b8d2a-aa3a-4114-a9e8-22a21549fdc8" />

<img width="1416" height="560" alt="image" src="https://github.com/user-attachments/assets/e54c2c25-f348-4764-8257-82c843681e4f" />

<img width="1413" height="611" alt="image" src="https://github.com/user-attachments/assets/c59a1dfa-1ad2-43e1-abae-818ba96a0440" />


# $${\color{red}{\textbf{⚠️ Problems With Traditional Setup}}}$$

❌ ${\color{red}{\textbf{Environment issues}}}$
❌ ${\color{red}{\textbf{Version mismatch}}}$
❌ ${\color{red}{\textbf{Dependencies not installed}}}$
❌ ${\color{red}{\textbf{"Works on my machine" problem}}}$
❌ ${\color{red}{\textbf{Time-consuming setup}}}$

---

# $${\color{lightblue}{\textbf{✅ Solution → Docker}}}$$

## $${\color{cyan}{\textbf{📌 What is Docker?}}}$$

${\color{lightblue}{\textbf{Docker}}}$ is an **open-source containerization platform** used for:

* Packaging applications
* Packaging dependencies
* Running the same setup across all environments

### $${\color{Green}{\textbf{✨ Benefits of Docker}}}$$

* ✔ ${\color{Green}{Portability}}$
* ✔ ${\color{Green}{Consistency}}$
* ✔ ${\color{Green}{Scalability}}$
* ✔ ${\color{Green}{Faster deployments}}$
* ✔ ${\color{Green}{Resource efficiency}}$


---

# $${\color{cyan}{\textbf{📌 Docker Workflow}}}$$

```
Dockerfile → Docker Image → Container
```

---

## $${\color{lightgreen}{\textbf{1️⃣ Dockerfile}}}$$

A text file containing build instructions.

```dockerfile
FROM ubuntu
RUN  apt update -y
RUN  apt install apache2 -y
COPY index.html  /var/www/html/
CMD ["apachectl", "-D", "FOREGROUND"]
```

---

## $${\color{lightgreen}{\textbf{2️⃣ Docker Image}}}$$

A **template** that includes:

* Code
* Dependencies
* Runtime
* Configurations

---

## $${\color{lightgreen}{\textbf{4️⃣ Container}}}$$

A **running instance** of a Docker image.

---

# $${\color{cyan}{\textbf{📌 Docker Across All Environments}}}$$

Before Docker:
Environment → Install software manually (slow & error-prone)

With Docker:
Same image → Same result → No mismatch ✔


##  ${\color{lightblue} \textbf{Installation-Steps  \ (Ubuntu)}}$ 


````
sudo apt update -y
sudo apt install  docker.io -y
sudo systemctl start docker
sudo systemctl enable docker
sudo usermod -aG docker ubuntu
newgrp docker
sudo chmod 777 /var/run/docker.sock
````
````
docker --version
````

## example:
- Dockerfile
- vim Dockerfile
````
```dockerfile
FROM ubuntu
RUN  apt update -y
RUN  apt install apache2 -y
COPY index.html  /var/www/html/
CMD ["apachectl", "-D", "FOREGROUND"]
```
- Docker Image
````
docker build -t image1 .
````
- list docker images
````
docker images
````
- Docker Container
````
docker run -itd --name cont1 -p 80:80 image1
````
- list running containers
````
docker ps
````


