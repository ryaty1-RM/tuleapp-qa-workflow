# Plan de Pruebas - QA Workflow

## 1. Objetivo

Validar el correcto funcionamiento del sistema de gestión de proyectos mediante pruebas funcionales y de gestión de tickets.

## 2. Alcance

- Gestión de tickets y bugs
- Flujo de trabajo kanban
- Trazabilidad de requisitos a casos de prueba

## 3. Tipos de Prueba

| Tipo       | Descripción                                                        |
| ---------- | ------------------------------------------------------------------ |
| Funcional  | Verificar que las funcionalidades principales operan correctamente |
| Regresión  | Asegurar que cambios no afecten funcionalidades existentes         |
| Aceptación | Validar que el sistema cumple los requisitos del usuario           |

## 4. Criterios de Entrada

- Board kanban configurado con columnas: Nuevo, En Proceso, Listo para prueba, Hecho
- Usuario con permisos de reporte creado
- Proyecto de prueba configurado

## 5. Criterios de Salida

- 100% de casos de prueba ejecutados
- 0 bugs críticos abiertos
- Documentación actualizada

## 6. Casos de Prueba

### CT-001 - Crear ticket

| Campo              | Detalle                                                             |
| ------------------ | ------------------------------------------------------------------- |
| ID                 | CT-001                                                              |
| Título             | Crear nuevo ticket de bug                                           |
| Precondición       | Usuario logueado con permisos de reporte                            |
| Pasos              | 1. Ir a board → 2. Click en Nuevo → 3. Llenar campos → 4. Guardar   |
| Resultado esperado | Ticket creado y visible en el tablero                               |
| Resultado actual   | ✅ Passed                                                           |
| Requisito          | REQ-001                                                             |
| Repo relacionado   | [cypress-saucedemo](https://github.com/ryaty1-RM/cypress-saucedemo) |

### CT-002 - Mover ticket entre estados

| Campo              | Detalle                                                                               |
| ------------------ | ------------------------------------------------------------------------------------- |
| ID                 | CT-002                                                                                |
| Título             | Mover ticket de Nuevo a En Proceso                                                    |
| Precondición       | Ticket CT-001 creado                                                                  |
| Pasos              | 1. Abrir ticket → 2. Arrastrar a columna En Proceso → 3. Verificar cambio             |
| Resultado esperado | Estado actualizado correctamente                                                      |
| Resultado actual   | ✅ Passed                                                                             |
| Requisito          | REQ-002                                                                               |
| Repo relacionado   | [jenkins-devsecops-pipeline](https://github.com/ryaty1-RM/jenkins-devsecops-pipeline) |

### CT-003 - Cerrar ticket resuelto

| Campo              | Detalle                                                                 |
| ------------------ | ----------------------------------------------------------------------- |
| ID                 | CT-003                                                                  |
| Título             | Mover ticket a Hecho                                                    |
| Precondición       | Ticket en estado En Proceso                                             |
| Pasos              | 1. Abrir ticket → 2. Arrastrar a columna Hecho → 3. Verificar           |
| Resultado esperado | Ticket cerrado y archivado                                              |
| Resultado actual   | ✅ Passed                                                               |
| Requisito          | REQ-003                                                                 |
| Repo relacionado   | [tuleapp-qa-workflow](https://github.com/ryaty1-RM/tuleapp-qa-workflow) |

---

## 7. Template - Bug Report

| Campo                 | Detalle                                  |
| --------------------- | ---------------------------------------- |
| ID                    | BUG-XXX                                  |
| Título                | Descripción corta del problema           |
| Severidad             | Alta / Media / Baja                      |
| Pasos para reproducir | 1. Paso uno → 2. Paso dos → 3. Paso tres |
| Resultado esperado    | Lo que debería pasar                     |
| Resultado actual      | Lo que realmente pasa                    |
| Estado                | Abierto / En proceso / Cerrado           |

### Ejemplo - BUG-001

| Campo                 | Detalle                                                |
| --------------------- | ------------------------------------------------------ |
| ID                    | BUG-001                                                |
| Título                | Formulario no valida campo email vacío                 |
| Severidad             | Media                                                  |
| Pasos para reproducir | 1. Ir a formulario → 2. Dejar email vacío → 3. Guardar |
| Resultado esperado    | Mensaje de error de validación                         |
| Resultado actual      | Formulario se envía sin validar                        |
| Estado                | Abierto                                                |

---

## 8. Template - Caso de Prueba

| Campo              | Detalle                   |
| ------------------ | ------------------------- |
| ID                 | CT-XXX                    |
| Título             | Nombre del caso de prueba |
| Precondiciones     | Estado inicial requerido  |
| Pasos              | 1. Paso uno → 2. Paso dos |
| Resultado esperado | Criterio de éxito         |
| Resultado actual   | ✅ Passed / ❌ Failed     |
| Requisito          | REQ-XXX                   |
| Repo relacionado   | Link al repositorio       |

---

## 9. Trazabilidad Requisitos → Tests

| Requisito | Descripción        | Caso de Prueba | Repositorio                                                                           |
| --------- | ------------------ | -------------- | ------------------------------------------------------------------------------------- |
| REQ-001   | Automatización E2E | CT-001         | [cypress-saucedemo](https://github.com/ryaty1-RM/cypress-saucedemo)                   |
| REQ-002   | Pipeline CI/CD     | CT-002         | [jenkins-devsecops-pipeline](https://github.com/ryaty1-RM/jenkins-devsecops-pipeline) |
| REQ-003   | Gestión QA         | CT-003         | [tuleapp-qa-workflow](https://github.com/ryaty1-RM/tuleapp-qa-workflow)               |
