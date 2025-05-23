# Authentication-Service

## Description
Comprehensive authentication and authorization service for SUPMAP that handles user registration,
email verification, secure password management, and OAuth2 social login integration. Provides JWT-based
authentication with metrics tracking for security monitoring, supports password reset workflows,
and ensures proper user identity management across the application ecosystem.

## Features
- User registration and account management
- Password reset functionality
- JWT-based authentication
- OAuth2 integration (Google, Facebook)
- Role-based access control
- Email verification
- Security monitoring and metrics

## Tech Stack
- Java 21
- Spring Boot 3.4.4
- Spring Security
- MongoDB for user data storage
- JWT for token-based authentication
- Kafka for event messaging
- Prometheus for monitoring

## Dependencies
- shared-models: Common data models across services
- database-utils: Database utility functions
- Spring Boot Security for authentication and authorization
- JJWT for JWT token generation and validation
- Spring Mail for email notifications
- Kafka for inter-service communication
- Prometheus for metrics collection

## Configuration
The service can be configured using environment variables:

```yaml
supmap:
 properties:
   app-email: your-app-email@example.com
   database-name: auth_service_db
   default-profile-image: /path/to/default/image.png
   elasticsearch-password: your-es-password
   elasticsearch-url: http://elasticsearch:9200
   elasticsearch-username: elastic
   jwt-secret: your-secret-key
   kafka-bootstrap-servers: kafka:9092
   mail-modified-username: modified-username
   mail-password: your-mail-password
   mongo-uri: mongodb://user:password@mongodb:27017/auth_service_db
   mail-register-confirmation-link: https://supmap.com/confirm-account
   reset-password-link: https://supmap.com/reset-password