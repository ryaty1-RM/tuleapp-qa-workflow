# TuleApp QA Workflow

Gestión de pruebas y trazabilidad de requisitos utilizando Taiga como herramienta de gestión de proyectos QA. Desarrollado como parte del curso de DevOps en la Universidad Mariano Gálvez de Guatemala.

---

## 📋 ¿Qué incluye?

- Tablero Kanban con tickets organizados por estado
- Plan de pruebas documentado
- Templates de bug report y casos de prueba
- Trazabilidad de requisitos a tests

---

## 🛠️ Tecnologías

![TuleApp](https://img.shields.io/badge/TuleApp-E4391D?style=for-the-badge&logoColor=white)
![QA](https://img.shields.io/badge/QA-Testing-green?style=for-the-badge)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)

---

## 📂 Estructura

tuleapp-qa-workflow/
├── docs/
│ └── plan-de-pruebas.md
├── screenshots/
└── docker-compose.yml

---

## 📸 Screenshots del tablero

![Board QA](https://raw.githubusercontent.com/ryaty1-RM/tuleapp-qa-workflow/main/screenshots/Captura%20de%20pantalla%202026-06-11%20155153.png)

---

## 📝 Templates

### Bug Report

| Campo                 | Descripción                    |
| --------------------- | ------------------------------ |
| ID                    | Identificador único del bug    |
| Título                | Descripción corta del problema |
| Severidad             | Alta / Media / Baja            |
| Pasos para reproducir | Lista de pasos                 |
| Resultado esperado    | Lo que debería pasar           |
| Resultado actual      | Lo que realmente pasa          |
| Estado                | Abierto / En proceso / Cerrado |

### Caso de Prueba

| Campo              | Descripción              |
| ------------------ | ------------------------ |
| ID                 | Identificador único      |
| Título             | Nombre del caso          |
| Precondiciones     | Estado inicial requerido |
| Pasos              | Acciones a ejecutar      |
| Resultado esperado | Criterio de éxito        |
| Requisito          | REQ-XXX                  |

---

## 📊 Trazabilidad Requisitos → Tests

| Requisito | Descripción        | Caso de Prueba | Repositorio                                                                           |
| --------- | ------------------ | -------------- | ------------------------------------------------------------------------------------- |
| REQ-001   | Automatización E2E | CT-001         | [cypress-saucedemo](https://github.com/ryaty1-RM/cypress-saucedemo)                   |
| REQ-002   | Pipeline CI/CD     | CT-002         | [jenkins-devsecops-pipeline](https://github.com/ryaty1-RM/jenkins-devsecops-pipeline) |
| REQ-003   | Gestión QA         | CT-003         | [tuleapp-qa-workflow](https://github.com/ryaty1-RM/tuleapp-qa-workflow)               |

---

## 🔗 Relacionado

Este proyecto se integra con el ecosistema DevSecOps:

| Repositorio                                                                           | Relación                                                                |
| ------------------------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| [cypress-saucedemo](https://github.com/ryaty1-RM/cypress-saucedemo)                   | Tests E2E automatizados relacionados a los casos de prueba documentados |
| [jenkins-devsecops-pipeline](https://github.com/ryaty1-RM/jenkins-devsecops-pipeline) | Pipeline CI/CD que ejecuta los tests y escaneos de seguridad            |

---

## 🌿 Estrategia de Branches

Este repositorio utiliza **GitHub Flow**:

| Branch    | Propósito                              |
| --------- | -------------------------------------- |
| `main`    | Código estable y listo para producción |
| `develop` | Rama de desarrollo e integración       |

**Flujo de trabajo:**

1. Todo el desarrollo se hace en `develop`
2. Cuando el código está listo y probado, se hace merge a `main`
3. `main` siempre contiene código funcional
