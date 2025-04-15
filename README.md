¡Vamos a dejar tu `README.md` profesional, claro y completo! Aquí tienes una versión documentada del archivo `README.md` para el proyecto **`sistema-educativo-microservicios`**:

---

```markdown
# 🎓 Sistema Educativo con Microservicios

Este proyecto es una arquitectura distribuida basada en **Spring Boot**, **Spring Cloud**, y **MongoDB**, que simula un sistema educativo dividido en microservicios.

## 📦 Estructura del Proyecto

```
sistema-educativo-microservicios/
├── usuarios-servicio/        # Gestión de estudiantes y docentes
├── asignaturas-servicio/     # Gestión de materias
├── matriculas-servicio/      # Matrícula de estudiantes
├── config-server/            # Servidor de configuración centralizado
├── eureka-server/            # Servidor de descubrimiento Eureka
├── config-repo/              # Archivos de configuración (Git)
├── docker-compose.yml        # Orquestación de servicios
└── .vscode/                  # Configuración para ejecución en VS Code
```

---

## 🧩 Microservicios

### 1. usuarios-servicio
Gestiona usuarios (estudiantes y docentes).  
Incluye autenticación con JWT.

### 2. asignaturas-servicio
Permite CRUD de materias, asociadas a docentes.

### 3. matriculas-servicio
Registra estudiantes en materias.  
Se comunica con los otros dos microservicios vía **Feign Client**.

---

## 🔐 Seguridad

El `usuarios-servicio` protege endpoints con **Spring Security + JWT**.  
Se definen roles (`ESTUDIANTE`, `DOCENTE`) y se generan tokens al iniciar sesión.

---

## 🔧 Infraestructura

- **Spring Cloud Config Server**: configuración centralizada para todos los servicios.
- **Eureka Server**: permite descubrir y registrar microservicios dinámicamente.
- **Feign Client**: usado en `matriculas-servicio` para integración entre servicios.

---

## 🐳 Docker

Se incluye un archivo `docker-compose.yml` que levanta todos los servicios:

```bash
docker-compose up --build
```

Incluye:
- MongoDB
- Eureka
- Config Server
- Todos los microservicios

---

## ⚙️ Requisitos

- Java 17
- Maven
- Docker y Docker Compose
- MongoDB (si no usas Docker)
- Visual Studio Code (opcional, con extensiones de Java)

---

## 🧪 Pruebas

Cada microservicio incluye pruebas unitarias básicas usando **Spring Boot Test**.  
También se proveen archivos de colección para Postman (no incluidos en esta versión).

---

## 🚀 Cómo Ejecutar

### Opción 1: Con Docker (recomendado)
```bash
docker-compose up --build
```

### Opción 2: Manual desde VS Code
1. Iniciar `config-server`
2. Iniciar `eureka-server`
3. Iniciar cada microservicio desde el panel de ejecución (ver `.vscode/launch.json`)

---

## 📊 Endpoints de Referencia

| Servicio         | Puerto | Endpoint de prueba                  |
|------------------|--------|-------------------------------------|
| Usuarios         | 8081   | `/api/usuarios`                    |
| Asignaturas      | 8082   | `/api/asignaturas`                |
| Matrículas       | 8083   | `/api/matriculas`                 |
| Eureka           | 8761   | `http://localhost:8761`           |
| Config Server    | 8888   | `http://localhost:8888`           |

---

## 🧠 Aprendizajes

Este proyecto demuestra:
- Separación de responsabilidades con microservicios
- Integración distribuida y comunicación interservicios
- Configuración centralizada y descubrimiento de servicios
- Autenticación y autorización en entornos distribuidos
- Orquestación con Docker

---


¡Gracias por revisar este proyecto!
```

