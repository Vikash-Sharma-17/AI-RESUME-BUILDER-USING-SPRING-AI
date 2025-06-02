# 🧠 Resume AI Backend

A Spring Boot-based backend application that generates professional IT job resumes from natural language descriptions using AI. It leverages [Spring AI](https://docs.spring.io/spring-ai/) and the `deepseek-r1` model via [Ollama](https://ollama.com/) for local inference.

---

## 🚀 Features

- 💬 Accepts user resume descriptions in plain text
- 🧠 Uses DeepSeek R1 LLM (via Ollama) to generate structured resume data
- 📄 Outputs a well-structured JSON resume including:
  - Personal Information
  - Summary
  - Skills
  - Experience
  - Education
  - Certifications
  - Projects
  - Achievements
  - Languages
  - Interests
- 📥 Template-based prompt system using external `.txt` files
- 🔧 Built with Spring Boot and Java 17+

---

## ⚙️ Tech Stack

- Java 17+
- Spring Boot 3.x
- Spring AI
- Ollama (Local LLM inference)
- DeepSeek R1 model (`deepseek-r1:latest`)
- Jackson for JSON parsing

---


## ⚙️ Configuration

Update your `application.properties`:

```properties
spring.application.name=resume-ai-backend
spring.ai.ollama.chat.model=deepseek-r1:latest

Ensure Ollama is installed and running on http://localhost:11434
Pull the model with:
ollama pull deepseek-r 

📜 Prompt Template (resume_prompt.txt)
Place this in src/main/resources/:

javascript
Copy
Edit
You are an expert resume generator.

Based on the following user description, return a professional IT job resume in the specified JSON structure.

Description:
{{userDescription}}

Return JSON only with the following structure:

personalInformation: Include the following keys:
fullName, email, phoneNumber, location, linkedIn, gitHub, portfolio

summary: String

skills: List of objects with keys 'title' and 'level'

experience: List with keys:
jobTitle, company, location, duration, responsibility

education: List with keys:
degree, university, location, graduationYear

certifications: List with keys:
title, issuingOrganization, year

projects: List with keys:
title, description, technologiesUsed (array), githubLink

achievements: List with keys:
title, year, extraInformation

languages: List with keys:
id, name

interests: List with keys:
id, name 
```
---

## 🧪 Output


![image](https://github.com/user-attachments/assets/8d5e755b-84e4-48ec-902c-4ac1c59fc76d)
![image](https://github.com/user-attachments/assets/9b66808b-babe-4804-988a-369e2bfd74c1)
![image](https://github.com/user-attachments/assets/691f73ea-7ffe-4965-8f22-b3d2335c5bd8)
![image](https://github.com/user-attachments/assets/769cfce0-6d8e-47b1-856a-a80dc0b75910)

### Postman Link
https://vikuuuuu-9124707.postman.co/workspace/Vikuuuuu's-Workspace~cf7d14d7-8808-45b8-8927-989a6c370742/request/44251648-b227dc05-9f38-4398-a8ce-8a068dbfc322?historyId=44251648-82e54582-8796-42eb-93aa-e0dae199dcc7&utm_source=postman&utm_medium=response_tab&utm_campaign=core&utm_content=link 

