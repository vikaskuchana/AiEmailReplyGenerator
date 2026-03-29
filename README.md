# 📧 AI Email Reply Generator (Spring Boot + Gemini)

An intelligent backend service built with Spring Boot that generates **context-aware, tone-specific email replies** using the Gemini LLM API.  
This project acts as a bridge between a frontend application and AI-powered email generation.

---

## 🚀 Features

- Generate professional email replies using AI  
- Tone customization (Professional, Friendly, etc.)  
- RESTful API for easy frontend integration  
- CORS enabled for cross-origin requests  
- Lightweight and scalable backend  

---

## 🛠️ Tech Stack

- Spring Boot  
- Gemini API  
- REST APIs  
- Lombok  
- Maven  
- WebClient  

---

## 📋 API Documentation

### Generate Email Reply

**Endpoint**
POST /api/email/generate


**Content-Type**

application/json


### Request Body

```json
{
  "emailContent": "Original email text here...",
  "tone": "Professional"
}
Response
Dear [Name],
Thank you for your email...
⚙️ Configuration

Add the following in application.properties:

spring.application.name=email-writer-sb

gemini.api.url=${GEMINI_URL}
gemini.api.key=${GEMINI_KEY}
Environment Variables
export GEMINI_URL=https://generativelanguage.googleapis.com/v1/models/gemini-pro:generateContent?key=
export GEMINI_KEY=your_api_key_here
🏗️ Project Structure
src/main/java/com/email/writer/app

├── controller
│   └── EmailGeneratorController.java
│
├── service
│   └── EmailGeneratorService.java
│
├── dto
│   └── EmailRequest.java
│
└── AppApplication.java
🧠 How It Works
Client sends email content via API
Backend builds prompt
Request sent to Gemini API
AI generates reply
Response parsed and returned
▶️ Running the Application
1. Clone Repository
git clone https://github.com/yourusername/email-writer-backend.git
cd email-writer-backend
2. Build
mvn clean install
3. Run
mvn spring-boot:run
🌐 API URL
http://localhost:8080/api/email/generate
⚠️ Notes
Keep your API keys secure
Do not commit secrets to GitHub
Use environment variables
📈 Future Enhancements
JWT Authentication
Multi-language support
Async processing
UI Integration
🤝 Contributing
Fork the project
Create a branch (feature/your-feature)
Commit changes
Push and create PR
📄 License

MIT License
