# 🎓 Sistema Educativo con Microservicios

Este proyecto es una arquitectura distribuida basada en **Spring Boot**, **Spring Cloud**, y **MongoDB**, que simula un sistema educativo dividido en microservicios.

## 📦 Estructura del Proyecto

```
sistema-educativo-microservicios/
├── usuarios-servicio/
├── asignaturas-servicio/
├── matriculas-servicio/
├── config-server/
├── eureka-server/
├── config-repo/
├── docker-compose.yml
└── .vscode/
```

## 🧩 Microservicios

### 1. usuarios-servicio
Gestiona usuarios (estudiantes y docentes). Incluye autenticación con JWT.

### 2. asignaturas-servicio
Permite CRUD de materias.

### 3. matriculas-servicio
Registra estudiantes en materias y se comunica con los otros microservicios vía **Feign Client**.

## 🔐 Seguridad

El `usuarios-servicio` protege endpoints con **Spring Security + JWT**.

## 🔧 Infraestructura

- **Spring Cloud Config Server**
- **Eureka Server**
- **Feign Client**

## 🐳 Docker

```bash
docker-compose up --build
```

## ⚙️ Requisitos

- Java 17
- Maven
- Docker
- VS Code (extensiones de Java)

## 🧪 Pruebas

Incluye pruebas unitarias básicas con **Spring Boot Test**.

## 🚀 Cómo Ejecutar

### Opción 1: Docker
```bash
docker-compose up --build
```

### Opción 2: VS Code
Inicia los servicios desde `.vscode/launch.json`.

## 📊 Endpoints

| Servicio     | Puerto | Endpoint               |
|--------------|--------|------------------------|
| Usuarios     | 8081   | `/api/usuarios`        |
| Asignaturas  | 8082   | `/api/asignaturas`     |
| Matrículas   | 8083   | `/api/matriculas`      |
| Eureka       | 8761   | `http://localhost:8761`|
| Config Server| 8888   | `http://localhost:8888`|

## ✍️ Autor

- **Tu Nombre**
- uniremington / Lenguaje de programacion avanzado II
- Abril 2025


¡Gracias por revisar este proyecto!
