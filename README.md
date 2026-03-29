📧 AI Email Reply Generator (Spring Boot + Gemini)

An intelligent backend service built with Spring Boot that generates context-aware, tone-specific email replies using the Gemini API.
This project acts as a bridge between a frontend application and AI-powered email generation.

🚀 Features
✨ Generate professional email replies using AI
🎯 Tone customization (Professional, Friendly, etc.)
🔌 RESTful API for easy frontend integration
🌐 CORS enabled for cross-origin requests
⚡ Lightweight and scalable backend architecture
🛠️ Tech Stack
Spring Boot
Gemini API
REST APIs
Lombok
Maven
WebClient (Spring Reactive)
📋 API Documentation
🔹 Generate Email Reply

Endpoint:

POST /api/email/generate

Content-Type:

application/json
✅ Request Body
{
  "emailContent": "Original email text here...",
  "tone": "Professional"
}
✅ Response
Dear [Name],
Thank you for your email...
⚙️ Configuration

Set your Gemini API credentials using environment variables:

spring.application.name=email-writer-sb

gemini.api.url=${GEMINI_URL}
gemini.api.key=${GEMINI_KEY}
🔐 Example (Local Setup)
export GEMINI_URL=https://generativelanguage.googleapis.com/v1/models/gemini-pro:generateContent?key=
export GEMINI_KEY=your_api_key_here
🏗️ Project Structure
src/main/java/com/email/writer/app
│
├── controller
│   └── EmailGeneratorController.java   # Handles API requests
│
├── service
│   └── EmailGeneratorService.java      # AI integration logic
│
├── dto
│   └── EmailRequest.java               # Request payload
│
└── Application.java                   # Main Spring Boot app
🧠 How It Works
User sends email content via REST API
Backend builds a structured prompt
Request is sent to Gemini API
AI generates response
Response is parsed and returned to client
▶️ Running the Application
1️⃣ Clone Repository
git clone https://github.com/yourusername/email-writer-backend.git
cd email-writer-backend
2️⃣ Build Project
mvn clean install
3️⃣ Run Application
mvn spring-boot:run
🌐 Access API
http://localhost:8080/api/email/generate
⚠️ Notes
Ensure your Gemini API key is valid
Do not expose API keys in public repositories
Use .env or environment variables for security
📈 Future Enhancements
Add authentication (JWT)
Email thread understanding
Multi-language support
Async processing for high scalability
UI integration
🤝 Contributing
Fork the repository
Create a new branch (feature/your-feature)
Commit your changes
Push and open a Pull Request
📄 License

This project is licensed under the MIT License.
