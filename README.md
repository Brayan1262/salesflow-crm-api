# SalesFlow CRM API

API REST tipo CRM desarrollada con Java Spring Boot para la gestión comercial de clientes, contactos, oportunidades de venta, actividades y dashboard empresarial.

---

## Descripción

SalesFlow CRM API es un sistema backend orientado a la gestión comercial de empresas. Permite registrar clientes, administrar contactos, controlar oportunidades de venta, programar actividades de seguimiento y visualizar indicadores clave mediante un dashboard CRM.

Este proyecto está inspirado en conceptos de plataformas CRM como Salesforce, aplicando arquitectura por capas, buenas prácticas REST, validaciones, manejo global de errores, documentación con Swagger y persistencia con PostgreSQL.

---

## Tecnologías utilizadas

- Java 21
- Spring Boot 3
- Spring Web
- Spring Data JPA
- Hibernate
- PostgreSQL
- Docker
- Docker Compose
- Lombok
- Bean Validation
- Swagger / OpenAPI
- Maven
- Git
- GitHub

---

## Funcionalidades principales

- Gestión de clientes.
- Gestión de contactos asociados a clientes.
- Gestión de oportunidades comerciales.
- Gestión de actividades y seguimientos.
- Dashboard CRM con indicadores comerciales.
- Validaciones de datos.
- Manejo global de errores.
- Documentación interactiva con Swagger.
- Base de datos PostgreSQL usando Docker.

---

## Módulos del sistema

### Clientes

Permite administrar empresas o clientes comerciales.

Endpoints principales:

```http
POST   /api/customers
GET    /api/customers
GET    /api/customers/{id}
GET    /api/customers/search?companyName=
GET    /api/customers/status/{status}
PUT    /api/customers/{id}
DELETE /api/customers/{id}

Estados disponibles:

ACTIVE
INACTIVE
PROSPECT
Contactos

Permite registrar personas de contacto asociadas a un cliente.

Endpoints principales:

POST   /api/contacts
GET    /api/contacts
GET    /api/contacts/{id}
GET    /api/contacts/customer/{customerId}
PUT    /api/contacts/{id}
DELETE /api/contacts/{id}
Oportunidades

Permite gestionar oportunidades de venta asociadas a clientes.

Endpoints principales:

POST   /api/opportunities
GET    /api/opportunities
GET    /api/opportunities/{id}
GET    /api/opportunities/customer/{customerId}
GET    /api/opportunities/status/{status}
PUT    /api/opportunities/{id}
DELETE /api/opportunities/{id}

Estados disponibles:

NEW
CONTACTED
PROPOSAL
NEGOTIATION
WON
LOST
Actividades

Permite registrar llamadas, reuniones, correos, tareas y notas comerciales.

Endpoints principales:

POST   /api/activities
GET    /api/activities
GET    /api/activities/{id}
GET    /api/activities/customer/{customerId}
GET    /api/activities/opportunity/{opportunityId}
GET    /api/activities/pending
PUT    /api/activities/{id}
PATCH  /api/activities/{id}/complete
DELETE /api/activities/{id}

Tipos disponibles:

CALL
EMAIL
MEETING
TASK
NOTE
Dashboard CRM

Muestra indicadores principales del sistema comercial.

Endpoint:

GET /api/dashboard

Indicadores incluidos:

Total de clientes.
Clientes activos.
Clientes prospectos.
Clientes inactivos.
Total de contactos.
Total de oportunidades.
Oportunidades abiertas.
Oportunidades ganadas.
Oportunidades perdidas.
Monto total estimado.
Monto ganado.
Total de actividades.
Actividades pendientes.
Actividades completadas.
Estructura del proyecto
salesflow-crm-api/
├── src/
│   ├── main/
│   │   ├── java/com/brayan/salesflow/
│   │   │   ├── config/
│   │   │   ├── controller/
│   │   │   ├── dto/
│   │   │   ├── entity/
│   │   │   ├── exception/
│   │   │   ├── repository/
│   │   │   └── service/
│   │   └── resources/
│   │       └── application.properties
│   └── test/
├── docker-compose.yml
├── pom.xml
├── README.md
└── .gitignore

Estado del proyecto
SalesFlow CRM API v1.0

Estado:

Funcional

Módulos completados:

Proyecto base.
PostgreSQL con Docker.
CRUD de clientes.
CRUD de contactos.
CRUD de oportunidades.
Gestión de actividades.
Dashboard CRM.
Validaciones.
Manejo global de errores.
Swagger / OpenAPI.
Futuras mejoras
Seguridad con JWT.
Roles ADMIN, SALES y SUPPORT.
Frontend Angular.
Reportes PDF.
Exportación Excel.
Auditoría de cambios.
Tests unitarios.
Despliegue en la nube.
Autor

Brayan Jair Chavez Oscor

GitHub: https://github.com/Brayan1262
LinkedIn: https://www.linkedin.com/in/brayan-chavez-218088334/
Portafolio: https://brayan1262.github.io/portafolio-brayan/