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

# $${\color{lightblue}{\textbf{📌 Application Example}}}$$

### $${\color{purple}{\textbf{Our Tech Stack}}}$$

* **Frontend:** React 19
* **Backend:** Java 17 + Tomcat 9.109
* **Database:** MariaDB 8.4

Docker allows each to run inside separate **containers**.

---

# $${\color{cyan}{\textbf{📌 Docker Workflow}}}$$

```
Dockerfile → Docker Image → DockerHub → Container
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

## $${\color{lightgreen}{\textbf{3️⃣ DockerHub}}}$$

A cloud **registry** to store and share images.

---

## $${\color{lightgreen}{\textbf{4️⃣ Container}}}$$

A **running instance** of a Docker image.

---

# $${\color{cyan}{\textbf{📌 Docker Across All Environments}}}$$

Before Docker:
Environment → Install software manually (slow & error-prone)

With Docker:
Environment → Install Docker → Run container → Done 🎯

```
DEV:   Instance → Docker → Image → Container
TEST:  Instance → Docker → Image → Container
UAT:   Instance → Docker → Image → Container
PROD:  Instance → Docker → Image → Container
```

Same image → Same result → No mismatch ✔


# Diff Monolithic vs Microservises Architecture
<img width="1281" height="601" alt="image" src="https://github.com/user-attachments/assets/b6704028-f9e4-4331-a65c-aff79077393a" />
<img width="1175" height="678" alt="image" src="https://github.com/user-attachments/assets/537434ed-6c7b-4d71-a247-bb61cfff4279" />
<img width="1285" height="575" alt="image" src="https://github.com/user-attachments/assets/6f20b98e-64a5-4ec5-a680-0740ee1b395e" />
<img width="1365" height="547" alt="image" src="https://github.com/user-attachments/assets/52c25be2-c2e0-4806-a3cb-b54636237476" />
<img width="1542" height="593" alt="image" src="https://github.com/user-attachments/assets/02800600-5a46-4ca0-9b17-8b6e76bbb625" />



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
