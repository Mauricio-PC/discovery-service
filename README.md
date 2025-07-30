
---

## 🔎 `discovery-service/README.md`


# 🧭 Discovery Service - Eureka Server

Este proyecto es el **Eureka Server** de la arquitectura **PokeMicroServicios**.  
Se encarga del **descubrimiento de servicios** para que cada microservicio (como `pokemon-service`) pueda encontrarse y comunicarse sin hardcodear direcciones.

---

## 🧰 Tecnologías

| Herramienta               | Descripción                              |
|---------------------------|------------------------------------------|
| 🧰 Spring Boot 2.7.18      | Framework principal                      |
| 🗺️ Spring Cloud Netflix Eureka Server | Componente central de descubrimiento |

---

## 🚀 ¿Qué hace?

- Actúa como un "registro telefónico" de los microservicios.
- Permite que los servicios se descubran dinámicamente.
- Ayuda al **API Gateway** a enrutar las peticiones sin direcciones fijas.

---

## 🌐 Acceso

Una vez levantado:
```yaml
http://localhost:8701/
```

Ahí verás los servicios registrados en vivo, como:

- `api-gateway`
- `pokemon-service`

---

## ⚙️ Configuración (`application.yml`)

```yaml
server:
  port: 8701

spring:
  application:
    name: discovery-service

eureka:
  client:
    register-with-eureka: false
    fetch-registry: false
```
register-with-eureka: false evita que el propio server se registre en sí mismo.

## 🧙 Autor
Creado por Mauricio-PC para el sistema PokeMicroServicios.
