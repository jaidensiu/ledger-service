# Ledger Service

![Gopher in a factory](images/go_factory.png)

A secure, scalable, and cloud-native backend service for managing bank accounts, transactions, and transfers.

## Objective

This project is built as part of a comprehensive backend engineering learning journey, implementing industry best practices and production-ready patterns. The goal is to design and implement a cloud-native financial service that demonstrates secure transaction processing, scalable architecture, and full observability, closely reflecting the challenges of real-world systems.

## Features

### Core Operations
- **Account Management**: Create and manage bank accounts with secure authentication
- **Transaction Recording**: Track all balance changes with complete audit trails
- **Money Transfers**: Execute secure transfers between accounts with proper validation
- **User Authentication**: JWT/PASETO token-based authentication system
- **Session Management**: Refresh token implementation for enhanced security

### API Capabilities
- **REST API**: Full-featured REST endpoints using Gin framework
- **gRPC Services**: High-performance gRPC APIs for internal services
- **Dual Protocol Support**: Serve both HTTP and gRPC simultaneously via gRPC Gateway
- **Swagger Documentation**: Auto-generated API documentation
- **Role-Based Access Control (RBAC)**: Fine-grained permission management

### Production-Grade Capabilities
- **Asynchronous Processing**: Background workers using Redis and Asynq
- **Email Notifications**: Email verification and notifications via Gmail SMTP
- **Structured Logging**: HTTP middleware and gRPC interceptors for comprehensive logging
- **Graceful Shutdown**: Proper resource cleanup and request handling during shutdown
- **Database Migrations**: Automated schema versioning and updates

## Roadmap

### Phase 1: Database Design
- Database schema design and generation
- CRUD operations with SQLC
- Database transactions and deadlock handling
- Transaction isolation configuration

### Phase 2: REST API Development
- HTTP API implementation with Gin
- Configuration management with Viper
- Custom parameter validation
- Password hashing with Bcrypt
- Token-based authentication (JWT/PASETO)
- Authorization middleware

### Phase 3: Cloud Deployment
- Docker containerization with multistage builds
- AWS EKS Kubernetes cluster setup
- Production database on AWS RDS
- Secrets management with AWS Secrets Manager
- Domain setup and TLS certificates (Let's Encrypt)
- CI/CD pipeline with GitHub Actions

### Phase 4: gRPC API Development
- gRPC API implementation
- gRPC Gateway integration
- gRPC API authorization
- gRPC interceptors and structured logging

### Phase 5: Event-Driven Architecture
- Redis-based message queue
- Background worker implementation
- SMTP client integration for mail service
- Transaction-aware async task distribution
- Comprehensive testing with mocked dependencies

### Phase 6: Security and Stability
- User session management with refresh tokens
- Enhanced cookie-based security
- Graceful shutdown mechanisms
- CORS policy configuration
- Role-based access control (RBAC)

### Phase 7: Observability and Monitoring
- Prometheus metrics collection and exposition
- Grafana dashboards for real-time monitoring
- Distributed tracing with OpenTelemetry
- Request latency and throughput tracking
- Database connection pool monitoring
- Error rate alerting and incident response
- Business metrics (transactions/sec, success rates)
- Health check endpoints for load balancers
- SLA tracking and performance baselines

## Tech Stack

### Language and Framework
- **Go/Golang**: Primary programming language
- **Gin**: HTTP web framework
- **gRPC**: High-performance RPC framework
- **Protocol Buffers**: API definition and serialization

### Database
- **PostgreSQL**: Primary relational database
- **SQLC**: Type-safe SQL code generation
- **PGX**: PostgreSQL driver

### Development Tools
- **Viper**: Configuration management
- **TablePlus**: Database management
- **k9s**: Kubernetes cluster management
- **Make**: Build automation
- **Postman**: API development and testing

### Documentation
- **Swagger/OpenAPI**: API documentation
- **Mermaid**: Diagramming and charting

### Authentication and Security
- **JWT**: JSON Web Tokens
- **PASETO**: Platform-Agnostic Security Tokens
- **Bcrypt**: Password hashing

### Asynchronous Processing
- **Redis**: Message broker and caching
- **Asynq**: Async task processing library

### Testing and Quality
- **GoMock**: Mocking framework
- **Testify**: Testing utilities
- **GitHub Actions**: CI/CD automation

### Infrastructure and DevOps
- **Docker**: Containerization
- **Docker Compose**: Local development orchestration
- **Kubernetes**: Container orchestration
- **AWS EKS**: Managed Kubernetes service
- **AWS RDS**: Managed PostgreSQL
- **AWS ECR**: Container registry
- **AWS Secrets Manager**: Secrets management
- **Let's Encrypt**: TLS certificate automation

### Observability and Monitoring

- **Prometheus**: Metrics collection and time-series database
- **Grafana**: Visualization and dashboarding platform
- **OpenTelemetry**: Distributed tracing and observability framework
