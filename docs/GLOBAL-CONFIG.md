# Configuración global

## Propósito

Este documento explica el rol de la configuración global de Codex y cómo se relaciona con la plantilla por proyecto.

## Archivos globales

### `~/.codex/AGENTS.md`
Usa este archivo para:
- reglas globales de ingeniería
- política de planificación
- modelo de colaboración
- contrato de salida
- expectativas de validación
- principios de activación de agentes

No metas aquí comandos ni estructura específica de repositorios.

### `~/.codex/config.toml`
Usa este archivo para:
- modelo por defecto
- esfuerzo de razonamiento
- sandbox mode
- approval policy
- concurrencia de agentes
- MCPs realmente reutilizables

### `~/.codex/agents/*.toml`
Usa este directorio para:
- agentes globales reutilizables
- definiciones de rol estables
- decisiones sobre herramientas
- skills permitidas
- restricciones por rol

## Catálogo global recomendado

- `project_manager`
- `frontend_developer`
- `backend_developer`
- `qa_engineer`
- `seo_performance_reviewer`
- `infra_devops`
- `documenter`
- `designer`
- `marketer`

## Estrategia global recomendada

### Mantener global
- roles reutilizables
- comportamiento estable
- reglas universales de calidad
- flujo global de colaboración
- preferencias personales

### Mantener por proyecto
- comandos
- detalles del stack
- estructura de carpetas
- MCPs específicos
- restricciones locales
- overrides especiales

## Enfoque sugerido para la config global

Usar la configuración global para:
- modelo por defecto
- esfuerzo de razonamiento
- `workspace-write` o el modo que prefieras
- `on-request` si quieres ejecución controlada
- `agents.max_threads` razonable
- `agents.max_depth = 1`

## Error común a evitar

No conviertas la capa global en un archivo gigante con reglas para todo. Eso hace que los agentes sean más ruidosos, genéricos y menos confiables.

La capa global debe ser una base estable, no un vertedero de excepciones.

## Skills vs instrucciones del agente

Usa instrucciones del agente para:
- identidad
- scope
- límites
- formato de salida
- política de decisión

Usa skills para:
- workflows reutilizables
- playbooks de planificación
- auditorías SEO
- rutinas de documentación
- tareas repetidas de ingeniería

Eso mantiene a los agentes más enfocados y eficientes.