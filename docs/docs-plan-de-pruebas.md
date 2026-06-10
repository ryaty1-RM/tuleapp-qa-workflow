# Plan de Pruebas - TuleApp QA Workflow

## 1. Objetivo

Validar el correcto funcionamiento del sistema de gestión de proyectos TuleApp mediante pruebas funcionales y de gestión de tickets.

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

- TuleApp levantado y accesible vía Docker
- Usuario administrador creado
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
| Pasos              | 1. Ir a tracker → 2. Click en Nuevo → 3. Llenar campos → 4. Guardar |
| Resultado esperado | Ticket creado y visible en el tablero                               |
| Resultado actual   | ✅ Passed                                                           |

### CT-002 - Mover ticket entre estados

| Campo  | Detalle                             |
| ------ | ----------------------------------- |
| ID     | CT-002                              |
| Título | Mover ticket de Nuevo a En Progreso |

|
