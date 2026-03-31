# Guía de plantilla de proyecto

## Propósito

Este documento explica cómo usar la plantilla de proyecto contenida en `templates/project-template/`.

## Archivos incluidos

```text
project-template/
├─ AGENTS.md
├─ .codex/
│  └─ config.toml
└─ docs/
   ├─ REQUIREMENTS.md
   ├─ ARCHITECTURE.md
   ├─ TEST_PLAN.md
   └─ RELEASE_NOTES.md
```

## Por qué existe esta plantilla

La plantilla convierte el sistema global de Codex en un modelo operativo específico por repositorio.

Captura:
- Qué es el proyecto
- Cómo está estructurado
- Cómo se ejecuta
- Qué restricciones importan
- Cómo deben comportarse los agentes localmente
- Qué artefactos debe tener el proyecto

## Cómo usarla

### Paso 1
Copiar la plantilla en un repositorio nuevo.

### Paso 2

Actualizar AGENTS.md con:
- Descripción
- Stack
- Stakeholders
- Carpetas
- Comandos
- Restricciones
- Flujo recomendado

### Paso 3

Actualizar .codex/config.toml con:
- MCPs específicos del repositorio
- Overrides si hacen falta

### Paso 4

Rellenar:
- docs/REQUIREMENTS.md
- docs/ARCHITECTURE.md
- docs/TEST_PLAN.md

### Paso 5

Usar project_manager para revisar y refinar el estado inicial del proyecto.

### Cuándo añadir agentes locales

Añade un agente local solo cuando:
- El repositorio tenga una especialización real
- El agente global se quede corto
- El proyecto necesite instrucciones dedicadas que no deben ir a nivel global

Ejemplos:
- database_specialist
- ads_integration_specialist
- crm_permissions_specialist

### Cuándo no añadir agentes locales

No añadas agentes locales solo porque suenan bien. Demasiados agentes generan solapamiento, confusión y malos handoffs.

## Política recomendada a nivel proyecto
- mantener AGENTS.md concreto
- mantener la config local pequeña
- mantener la documentación viva
- no duplicar todo el sistema global dentro del repositorio