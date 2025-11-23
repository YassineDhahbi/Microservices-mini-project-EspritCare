# 🏥 EspritCare – Architecture Microservices Moderne
### Mini-projet de fin de semestre – ESPRIT  
**Janvier 2025 → Avril 2025**


> Système complet de gestion hospitalière basé sur une **architecture microservices** ultra-moderne, résilient et scalable.  
> Projet réalisé à l’**ESPRIT – Ecole Supérieure Privée d’Ingénierie et de Technologies**.

[![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.3-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white)](https://spring.io/)
[![Angular](https://img.shields.io/badge/Angular-18-DD0031?style=for-the-badge&logo=angular&logoColor=white)](https://angular.io/)
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://docker.com/)
[![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)](https://mongodb.com/)
[![Keycloak](https://img.shields.io/badge/Keycloak-1.0-525DC3?style=for-the-badge&logo=keycloak&logoColor=white)](https://www.keycloak.org/)
[![Eureka](https://img.shields.io/badge/Eureka-2.0-6DB33F?style=for-the-badge&logo=spring&logoColor=white)](https://spring.io/projects/spring-cloud-netflix)

## 🛠 Architecture Microservices

| Service              | Technologie             | Base de données | Port   |
|----------------------|-------------------------|------------------|--------|
| `gateway-service`    | Spring Cloud Gateway    | –                | 8080   |
| `discovery-service`  | Netflix Eureka Server   | –                | 8761   |
| `patient-service`    | Spring Boot + JPA       | H2 (dev) / MySQL | 8200   |
| `appointment-service`| Spring Boot + Reactive  | MongoDB          | 8201   |
| `auth-service`       | Keycloak + Node.js/Express | Keycloak DB   | 8081   |
| `frontend`           | Angular 18              | –                | 4200   |

## 🚀 Fonctionnalités implémentées

- Découverte de services avec **Eureka Dashboard**
- Routage intelligent via **Spring Cloud Gateway**
- Authentification & autorisation centrale avec **Keycloak** (OAuth2 / OpenID Connect)
- API REST + Reactive (WebFlux) selon les services
- Persistance polyglotte : SQL (H2/MySQL) + NoSQL (MongoDB)
- Full **Dockerisé** avec Docker Compose
- Frontend Angular moderne (standalone components, signals)


## 🐳 Lancement ultra-simple avec Docker (recommandé)

```bash
# 1. Tout lancer en une seule commande
docker-compose up -d --build

# Services disponibles :
# Frontend      → http://localhost:4200
# API Gateway   → http://localhost:8080
# Eureka        → http://localhost:8761
# Keycloak      → http://localhost:8081 (admin/admin123)
# Mongo Express → http://localhost:8082
