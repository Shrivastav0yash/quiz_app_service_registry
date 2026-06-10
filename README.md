# Quiz App Service Registry

The Service Registry is a Spring Boot microservice that acts as the central registry for service discovery within the Quiz Application microservices ecosystem.

It uses Netflix Eureka Server to allow microservices to register themselves dynamically and discover other services without hardcoding hostnames or ports.

---

## Project Context

This repository contains the Service Registry for the Quiz Application.

Current Microservices:

- Service Registry ✅
- Question Service ✅
- Quiz Service 🚧 (In Development)

The Service Registry serves as the central hub where all microservices register themselves and discover other available services.

---

## Responsibilities

The Service Registry is responsible for:

- Service Registration
- Service Discovery
- Maintaining Service Instances
- Health Monitoring
- Dynamic Service Lookup
- Supporting Scalability

---

## Tech Stack

### Backend

- Java
- Spring Boot
- Spring Cloud

### Service Discovery

- Netflix Eureka Server

### Build Tool

- Maven

---

## Why Service Discovery?

In a microservices architecture, services may run on different ports, servers, or containers.

Instead of hardcoding service locations, services register themselves with Eureka and discover other services dynamically.

Benefits include:

- Loose Coupling
- Dynamic Scaling
- Better Fault Tolerance
- Easier Service Management
- Simplified Communication

---

## Architecture

```text
                 ┌─────────────────────┐
                 │  Service Registry   │
                 │   (Eureka Server)   │
                 └──────────┬──────────┘
                            │
        ┌───────────────────┼───────────────────┐
        │                   │                   │
        ▼                   ▼                   ▼

┌─────────────────┐ ┌─────────────────┐ ┌─────────────────┐
│ Question Service│ │   Quiz Service  │ │ Future Services │
└─────────────────┘ └─────────────────┘ └─────────────────┘
```

All microservices register with the Service Registry and can discover each other through Eureka.

---

## Features

- Eureka Server Configuration
- Service Registration
- Service Discovery
- Centralized Registry
- Dynamic Service Lookup
- Health Monitoring Dashboard

---

## Project Structure

```text
src
├── main
│   ├── java
│   └── resources
└── test
```

---

## Future Enhancements

As the Quiz Application ecosystem grows, the following components may be integrated:

- API Gateway
- OpenFeign Clients
- Distributed Tracing
- Centralized Configuration Server
- Docker Deployment
- Monitoring & Logging
- Kubernetes Deployment

---

## Learning Objectives

This project was built to gain practical experience with:

- Microservices Architecture
- Service Discovery
- Netflix Eureka
- Spring Cloud
- Distributed Systems
- Scalable Backend Development

---

## Author

**Yash Shrivastav**

Java Backend Developer focused on building scalable applications using Spring Boot, Microservices, and modern backend technologies.

---

## Note

This repository contains only the Service Registry (Eureka Server). It provides service discovery capabilities for the Quiz Application microservices ecosystem and enables seamless communication between independently deployed services.
