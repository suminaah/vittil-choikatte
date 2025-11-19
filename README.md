# vittil-choikatte


Permission Seeker – Java Web Application
A simple and fun Java EE web application where users enter their name and age, ask a question, and after a playful loading animation (“Asking your dad”, “Asking your mom”), the app always replies with NO.
Built using Maven, Servlets (J2EE/Jakarta), JSP, and PostgreSQL.
________________________________________
🚀 Features
•	Collect user name and age via a web form.
•	Store user details in a PostgreSQL database.
•	Next page accepts a question from the user.
•	Shows a 10‑second comedy loading animation.
•	Final response displayed: “NO”.
•	Fully Maven-based project structure.
•	Deployable on Tomcat.
________________________________________
📁 Project Structure
src/
  main/
    java/
      com.permissionseeker/
        model/
        dao/
        servlet/
    webapp/
      WEB-INF/
        web.xml
      index.jsp
      question.jsp
      result.jsp
________________________________________
🛠️ Technologies Used
•	Java 8+
•	JSP + Servlets
•	Maven
•	PostgreSQL
•	HTML/CSS/JS
•	Apache Tomcat (recommended version: 9+)
________________________________________
📦 Maven Dependencies
Add these to your pom.xml:
<dependencies>
    <dependency>
        <groupId>jakarta.servlet</groupId>
        <artifactId>jakarta.servlet-api</artifactId>
        <version>5.0.0</version>
        <scope>provided</scope>
    </dependency>

    <dependency>
        <groupId>org.postgresql</groupId>
        <artifactId>postgresql</artifactId>
        <version>42.6.0</version>
    </dependency>

    <dependency>
        <groupId>javax.servlet</groupId>
        <artifactId>jstl</artifactId>
        <version>1.2</version>
    </dependency>
</dependencies>
________________________________________
🗄️ Database Setup (PostgreSQL)
Run:
CREATE DATABASE permissiondb;

CREATE TABLE users (
    id SERIAL PRIMARY KEY,
    name VARCHAR(100),
    age INT
);
Update your DB credentials in UserDAO.java:
private static final String URL = "jdbc:postgresql://localhost:5432/permissiondb";
private static final String USER = "postgres";
private static final String PASSWORD = "your_password";
________________________________________
▶️ Running the Project
1. Build using Maven
mvn clean package
This generates a WAR file inside target/.
2. Deploy on Tomcat
Copy the WAR file to:
TOMCAT_HOME/webapps/
Start Tomcat, then open:
http://localhost:8080/permission-seeker
________________________________________
🧪 Application Flow
Step 1 — Index Page
Enter name and age → Data gets saved.
Step 2 — Question Page
Ask your question in a text box.
Step 3 — Fake Loading Page
A fun loading sequence for 10 seconds: - Asking your dad… - Asking your mom…
Final Output
NO
________________________________________
📤 GitHub Setup
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/yourusername/permission-seeker.git
git push -u origin main
________________________________________
📌 Future Enhancements
•	Add login system
•	Display all previously asked questions
•	Add animations using JavaScript
•	Convert backend to Spring Boot later
________________________________________
👩‍💻 Author
Fathima Sumina N

