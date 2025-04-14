# 🗨️ Chat Application - Spring Boot Backend

This is a simple chat application backend built using **Spring Boot**. It integrates with [ChatEngine.io](https://chatengine.io/) to manage chat users and sessions. The application exposes RESTful APIs for user authentication (`/login`) and registration (`/signup`).

---

## 📦 Tech Stack

- **Java 17**
- **Spring Boot 3.1.5**
- **Maven**
- **ChatEngine.io API**
- **Gson** & **org.json** for JSON handling

---

## 🚀 Getting Started

### Prerequisites

Make sure you have the following installed:

- Java 17
- Maven
- IDE (e.g., IntelliJ IDEA, Eclipse)

---

### 🔧 Setup & Run

1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-username/chatapplication.git
   cd chatapplication

2. Configure API Keys:
   Update UserController.java with your ChatEngine project credentials:
   private static String CHAT_ENGINE_PROJECT_ID = "<your-project-id>";  
   private static String CHAT_ENGINE_PRIVATE_KEY = "<your-private-key>";

3. Build and run the app:
   mvn spring-boot:run
   The application will start at: http://localhost:8080

---

📨 API Endpoints
🔐 POST /login
Validates a user with ChatEngine.

Request Body:  
{  
  "username": "exampleUser",  
  "secret": "userSecret"  
}  
Response:  
- 200 OK with user details  
- 400 Bad Request on failure  

---

📝 POST /signup
Creates a new user on ChatEngine.

Request Body:   
{  
  "username": "newUser",  
  "secret": "userSecret",  
  "email": "user@example.com",  
  "first_name": "John",  
  "last_name": "Doe"  
}  
Response:  
- 200 OK with created user info
- 400 Bad Request on failure

---

🔄 CORS Support  
The application includes @CrossOrigin annotations to enable cross-origin requests for frontend integration.  

🛠️ Dependencies
- spring-boot-starter-web
- spring-boot-devtools
- spring-boot-starter-test
- reactor-test
- gson
- org.json




