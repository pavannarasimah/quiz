QuizApp Microservices Architecture Overview
The project follows a microservices-based architecture with four main components:
1. API Gateway 
  •	Purpose: Routes client requests to the appropriate services and handles cross-cutting concerns like authentication.
  •	Key Files: 
    o	ApiGatewayApplication.java: The main entry point of the gateway.
    o	application.properties: Configuration settings for the gateway.
2. Question Service 
  •	Purpose: Manages quiz questions, including CRUD operations.
  •	Key Components: 
    o	controller/QuestionController.java: Handles REST APIs for questions.
    o	dao/QuestionDao.java: Data access layer for managing questions.
    o	model/Question.java, QuestionWrapper.java, Response.java: Defines data models.
    o	service/QuestionService.java: Business logic for handling questions.
3. Quiz Service 
  •	Purpose: Manages quiz creation, participation, and scoring.
  •	Key Components: 
    o	controller/QuizController.java: Handles quiz-related REST APIs.
    o	dao/QuizDao.java: Data access layer for quizzes.
    o	feign/QuizInterface.java: Handles inter-service communication (Feign Client).
    o	model/Quiz.java, QuizDto.java, QuestionWrapper.java: Defines quiz models.
    o	service/QuizService.java: Business logic for quiz management.
4. Service Registry
  •	Purpose: Implements service discovery using Eureka Server, enabling dynamic service registration and discovery.
  •	Key File: 
    o	ServiceRegistoryApplication.java: Main class running the Eureka server.
Tech Stack & Tools Used
    •	Language: Java
    •	Framework: Spring Boot
    •	Service Discovery: Eureka Server
    •	Build Tool: Maven
    •	Inter-Service Communication: Feign Client
