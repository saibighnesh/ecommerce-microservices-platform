# Cloud-Native E-Commerce Microservices Platform

A comprehensive demonstration of microservices architecture, API design, and cloud-native patterns for building scalable e-commerce solutions.

## 🏗️ Architecture Overview

This project showcases a production-ready e-commerce platform built with microservices architecture, implementing industry best practices for cloud-native applications.

### System Architecture

```
                    ┌─────────────────────────────────┐
                    │   API Gateway (Kong/Nginx)      │
                    └──────────────┬──────────────────┘
                                   │
        ┌──────────────────────────┼──────────────────────────┐
        │                          │                          │
┌───────▼──────────┐    ┌─────────▼────────┐    ┌──────────▼─────────┐
│  User Service    │    │ Product Service  │    │   Order Service    │
│  (SpringBoot)    │    │  (FastAPI)       │    │   (SpringBoot)     │
│  Port: 8081      │    │  Port: 8082      │    │   Port: 8083       │
└───────┬──────────┘    └─────────┬────────┘    └──────────┬─────────┘
        │                          │                        │
        └──────────────────────────┼────────────────────────┘
                                   │
                        ┌──────────▼──────────┐
                        │   Apache Kafka      │
                        │  (Event Streaming)  │
                        └──────────┬──────────┘
                                   │
        ┌──────────────────────────┼──────────────────────────┐
        │                          │                          │
┌───────▼──────────┐    ┌─────────▼────────┐    ┌──────────▼─────────┐
│ Payment Service  │    │ Notification Svc │    │ Inventory Service  │
│   (FastAPI)      │    │   (FastAPI)      │    │   (SpringBoot)     │
│  Port: 8084      │    │  Port: 8086      │    │   Port: 8085       │
└──────────────────┘    └──────────────────┘    └────────────────────┘
```

## 🎯 Key Features

### Architecture Patterns
- **Microservices Architecture**: 8+ independently deployable services
- **Event-Driven Communication**: Apache Kafka for asynchronous messaging
- **Domain-Driven Design**: Clear bounded contexts
- **API Gateway Pattern**: Centralized routing and authentication
- **Circuit Breaker**: Resilience4j for fault tolerance
- **CQRS**: Command Query Responsibility Segregation

### Technology Stack

**Backend Services:**
- Java SpringBoot 3.x
- Python FastAPI 0.100+
- REST APIs with OpenAPI/Swagger

**Data Storage:**
- PostgreSQL (Transactional data)
- MongoDB (Product catalog)
- Redis (Caching & Sessions)
- Elasticsearch (Search)

**Messaging:**
- Apache Kafka (Event streaming)

**Infrastructure:**
- Docker & Kubernetes
- Terraform (IaC)
- AWS: EC2, S3, Lambda, RDS, EKS

**CI/CD:**
- Jenkins & GitHub Actions
- Prometheus & Grafana

## 📋 Microservices

| Service | Technology | Port | Purpose |
|---------|-----------|------|----------|
| User Management | Java SpringBoot | 8081 | Authentication, user profiles |
| Product Catalog | Python FastAPI | 8082 | Product CRUD, search |
| Order Service | Java SpringBoot | 8083 | Order processing |
| Payment Service | Python FastAPI | 8084 | Payment processing |
| Inventory Service | Java SpringBoot | 8085 | Stock management |
| Notification Service | Python FastAPI | 8086 | Email/SMS notifications |
| Cart Service | Java SpringBoot | 8087 | Shopping cart (Redis) |
| Review Service | Python FastAPI | 8088 | Product reviews |

## 📁 Repository Structure

```
.
├── docs/                              # Architecture documentation
│   ├── high-level-design.md           # HLD document
│   ├── api-contracts.md               # API specifications
│   └── data-models.md                 # Database schemas
├── infrastructure/                    # Infrastructure as Code
│   ├── terraform/                     # AWS Terraform configs
│   └── kubernetes/                    # K8s manifests
└── README.md
```

## 🏛️ Documentation

- [High-Level Design](docs/high-level-design.md) - System architecture and design principles
- [API Contracts](docs/api-contracts.md) - REST API specifications
- [Data Models](docs/data-models.md) - Database schemas

## 🎓 Learning Outcomes

This project demonstrates:
✅ Solution architecture and system design  
✅ Microservices patterns and best practices  
✅ Cloud-native application development  
✅ Infrastructure as Code (Terraform)  
✅ CI/CD pipeline design  
✅ Event-driven architecture with Kafka  
✅ API design and documentation  
✅ Observability and monitoring  

## 👤 Author

**Simadri Sai Bighnesh Prusty**
