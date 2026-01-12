# AyurEssence – Ayurvedic Diet Management Platform

A web application designed to help Ayurvedic dietitians manage patients and generate personalized, Ayurveda-compliant diet plans by integrating traditional principles with modern nutritional science.

## Table of Contents
**Overview**
**Architecture**
**Tech Stack**
**Features**
**Swagger Documentation**
**Application Setup**
**API Endpoints**
**Database Design**
**License**

## Overview

AyurEssence is a healthcare-focused platform built for Ayurvedic dietitians to efficiently manage patient records, appointments, and personalized diet charts.
The system generates automated diet plans based on age, gender, and health parameters, while integrating Ayurvedic concepts such as food properties and tastes with modern nutritional metrics like calories and macronutrients.
The application aims to bridge the gap between traditional Ayurveda and contemporary diet planning systems through a structured, scalable, and technology-driven approach.

## Architecture

The React frontend consumes REST APIs exposed by the Spring Boot backend.
The backend handles business logic, diet chart generation, and data persistence.
PostgreSQL is used for structured and relational data storage.

## Tech Stack

**Frontend:** React
**Backend:** Spring Boot (Java)
**Database:** PostgreSQL
**API Documentation:** Swagger (Springdoc OpenAPI)
**Build Tools:** Maven, npm

## Features

- Platform for Ayurvedic dietitians to manage patients and appointments
- Automated generation of personalized diet charts based on:
  - Age
  - Gender
  - Health parameters
- Integration of modern nutritional metrics:
  - Calories
  - Macronutrients (proteins, fats, carbohydrates)
- Integration of Ayurvedic principles:
  - Hot/Cold food properties
  - Six tastes (Rasa)
  - Digestibility considerations
- Role-based REST APIs for dietitians and patients
- Scalable PostgreSQL schema for healthcare data management

## API Documentation (Swagger)

Swagger UI is integrated using Springdoc OpenAPI.
Access Swagger UI at:
http://localhost:8080/swagger-ui.html
Swagger provides:
- Interactive API testing
- Request/response models
- HTTP status codes
- Schema definitions

**Swagger Features**
Interactive exploration of all REST APIs
Detailed request and response schemas
HTTP response codes and descriptions
Easy testing of endpoints directly from the browser
The documentation is automatically generated using Springdoc OpenAPI annotations.

**Application Setup**
Prerequisites
Java 17 or above
Node.js and npm
PostgreSQL
Maven

## Backend Setup (Spring Boot)
Clone the repository:
git clone <repository-url>
cd ayuressence-backend

Configure PostgreSQL credentials in application.properties:
spring.datasource.url=jdbc:postgresql://localhost:5432/ayuressence
spring.datasource.username=your_username
spring.datasource.password=your_password

Build and run the backend:
mvn clean install
mvn spring-boot:run

Frontend Setup (React)
Navigate to the frontend directory:
cd ayuressence-frontend

Install dependencies:
npm install

Start the React application:
npm start

## Backend (Spring Boot)
Exposes RESTful APIs for:
Patient management
Dietitian dashboards
Diet chart generation and modification
Food and nutrition data access
Implements business logic for Ayurveda-compliant diet planning
Uses PostgreSQL for persistent data storage

## Frontend (React)
Provides user interfaces for dietitians and patients
Displays dashboards, diet charts, and appointment details
Communicates with the backend using REST APIs

## API Endpoints (High Level)
**Authentication**
POST /api/auth/signup
POST /api/auth/login

**Dietitian**
Manage patients and appointments
Generate and update diet charts
View dashboards and analytics

**Patient**
Submit health parameters
View assigned diet charts
Track appointments

All endpoints are fully documented in Swagger UI.

## Database Design
The PostgreSQL database schema is structured to efficiently manage:
Users (Dietitians and Patients)
Patient health parameters
Food items with nutritional attributes
Ayurvedic properties (Rasa, digestibility, hot/cold nature)
Meals and diet charts
Appointments and dashboards
The schema is normalized to ensure data consistency, scalability, and maintainability.

## License
This project is licensed under the MIT License. See the LICENSE file for details.
