# Secret Santa Generator Application :santa:(CI/CD with docker)

A __secret santa generator web application__ built using __Spring Boot technologies__, __Thymeleaf views__, __JPA__, __H2 Database__, and more. The project features Spring Model, View, and Controller (MVC) architecture and Service and Repository layers.

This project is based on the popular Christmas game __Secret Santa__ where friends draw names from a hat to decide who they are required to give a present to. This project allows users to add names, and the project randomly generates secret santa matches (it isn't as simple as creating random pairs). There are different solutions to the "Secret Santa problem" as the problem essentially creates a directed graph. 

**Preview images** :small_red_triangle_down:
<details>
<summary>Some images of the application </summary>

* Welcome Page

![Welcome](https://github.com/NotTheBest/secretsanta-generator/blob/master/preview-images/welcomepage.png?raw=true)

* Add People

![Add](https://github.com/NotTheBest/secretsanta-generator/blob/master/preview-images/addpage.png?raw=true)

* Generate "Matches"

![Matches](https://github.com/NotTheBest/secretsanta-generator/blob/master/preview-images/generatepage.png?raw=true)

</details>


You can then access the application here: http://<ip>:8080/

![Welcome](https://github.com/NotTheBest/secretsanta-generator/blob/master/preview-images/welcomepage.png?raw=true)

# 🚀 CI/CD Pipeline for Java Application

This project implements a professional CI/CD pipeline using **Jenkins** for a Java-based application. The pipeline automates code compilation, testing, static code analysis, security vulnerability scanning, and containerization. This ensures fast, reliable, and secure delivery of software.

---
✅ Prerequisites
Make sure these are installed before starting:
-Git
- Docker
- Jenkins (or use Jenkins Docker container)
- Java JDK 17+ (configured in Jenkins)
- Apache Maven (configured in Jenkins)
- SonarQube (running separately, configured in Jenkins)
- OWASP Dependency-Check CLI (configured in Jenkins)


## 📌 Key Features

- 🔁 Automated Git Checkout
- ☕ Build & Test using **Maven**
- 🧠 Code Quality Analysis with **SonarQube**
- 🔒 Dependency Vulnerability Scanning using **OWASP Dependency-Check**
- 🐳 Docker Image Build
- ✅ Ready for Deployment

---
## 🛠️ Tech Stack / Tools Used

```text
1️⃣ Git Checkout       -> Pull code from GitHub
2️⃣ Maven Compile      -> Build and compile the Java application
3️⃣ Unit Testing       -> Execute tests (if present)
4️⃣ SonarQube Analysis -> Analyze code quality
5️⃣ OWASP Scan         -> Identify vulnerable dependencies
6️⃣ Docker Build       -> Build Docker image of the application
7️⃣ Deploy (Optional)  -> Ready for deployment to staging/production
```
🚀 How to Run the Pipeline
🔧 Step 1: Clone the Project
```
git clone https://github.com/p-udaykiran/secretsanta-generator.git
cd secretsanta-generator
```
🐳 Step 2: Start Docker
```
sudo systemctl start docker     # For Linux systems
```

⚙️ Step 3: Start Jenkins
If Jenkins is installed locally:
```
sudo systemctl start jenkins
```

🛠️ Step 4: Configure Jenkins
You need to do this only once during initial setup.
Install Required Plugins (Manage Jenkins → Plugin Manager):
1. Pipeline
2. Git
3. Docker Pipeline
4. SonarQube Scanner
5. OWASP Dependency-Check Plugin
---
Global Tool Configuration (Manage Jenkins → Global Tool Configuration):
1. JDK → Name: jdk17(17 version)
2. Maven → Name: maven3(latest)
3. SonarQube → Name: MySonarQube
4. Sonar Scanner → Name: sonar_scanner(6th version)
5. Dependency-Check → Name: DC(latest)
---
🧱 Step 5: Create a Jenkins Pipeline Job
1. Click New Item
2. Name your job (e.g., Java-CICD)
3. Choose Pipeline
4. Under Pipeline Definition, select:
5. Pipeline script from SCM
6. SCM: Git
```
Repo URL: https://github.com/p-udaykiran/secretsanta-generator.git
Branch: master
```
7. Script Path: Jenkinsfile
---
▶️ Step 6: Run the Pipeline
Click on Build Now.<br>
Jenkins will automatically go through these stages:

| Stage           | Description                       |
| --------------- | --------------------------------- |
| 🔁 Git Checkout | Clones the latest code            |
| ☕ Maven Build   | Compiles the app using Maven      |
| 🧠 SonarQube    | Analyzes code quality             |
| 🔐 OWASP        | Scans for vulnerable dependencies |
| 🐳 Docker Build | Builds Docker image of the app    |

---
🔍 Step 7: CI/CD
---
![App Preview](preview-images/Screenshot%20from%202025-06-29%2020-53-18.png)
![App Preview](preview-images/cicd(java_app).png)





