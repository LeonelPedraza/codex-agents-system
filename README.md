# Codex Agent System

Sistema estructurado y reutilizable de agentes para Codex CLI, diseñado para trabajar como un equipo técnico especializado en paralelo en lugar de depender de una sola sesión secuencial.

## Objetivo

Este repositorio define una forma práctica de trabajar con Codex CLI usando:

- subagentes especializados
- configuración global reutilizable
- configuración específica por proyecto
- plantillas repetibles para nuevos repositorios
- flujos claros de planificación, implementación, testing y documentación

## Idea principal

El sistema se apoya en cuatro capas:

1. guía global en `~/.codex/AGENTS.md`
2. configuración global en `~/.codex/config.toml`
3. subagentes globales en `~/.codex/agents/*.toml`
4. plantillas por proyecto con `AGENTS.md`, `.codex/config.toml` y documentación local

Esto permite tener una base estable y reutilizable, pero adaptar cada proyecto a su stack, reglas y herramientas reales.

## Catálogo de agentes

El catálogo global recomendado es:

- `project_manager`
- `frontend_developer`
- `backend_developer`
- `qa_engineer`
- `seo_performance_reviewer`
- `infra_devops`
- `documenter`
- `designer`
- `marketer`

### Núcleo recomendado
- Project Manager
- Frontend Developer
- Backend Developer
- QA Engineer
- Infra / DevOps
- Documenter

### Agentes condicionales
- SEO & Performance Reviewer
- Designer
- Marketer

## Principios del sistema

- agentes estrechos y especializados
- una tarea coherente por thread
- no poner varios agentes a editar los mismos archivos al mismo tiempo
- planificar primero cuando el trabajo es ambiguo, grande o arriesgado
- mantener lo global reutilizable
- mover lo específico al proyecto
- usar skills para workflows repetibles
- mantener la documentación alineada con el comportamiento real del sistema

## Estructura del repositorio

```text
├─ README.md
├─ SETUP.md
├─ docs/
│  ├─ ARCHITECTURE.md
│  ├─ GLOBAL-CONFIG.md
│  ├─ AGENT-CATALOG.md
│  └─ PROJECT-TEMPLATE.md
└─ templates/
   └─ project-template/
      ├─ AGENTS.md
      ├─ .codex/
      │  └─ config.toml
      └─ docs/
         ├─ REQUIREMENTS.md
         ├─ ARCHITECTURE.md
         ├─ TEST_PLAN.md
         └─ RELEASE_NOTES.md
```

## Estructura global recomendada en tu máquina

```text
~/.codex/
├─ AGENTS.md
├─ config.toml
├─ agents/
│  ├─ project_manager.toml
│  ├─ frontend_developer.toml
│  ├─ backend_developer.toml
│  ├─ qa_engineer.toml
│  ├─ seo_performance_reviewer.toml
│  ├─ infra_devops.toml
│  ├─ documenter.toml
│  ├─ designer.toml
│  └─ marketer.toml
└─ skills/
```

## Qué va en global y qué va por proyecto

### Global
Usa la configuración global para:

- Catálogo base de agentes
- Reglas universales
- Formato de salida
- Colaboración entre agentes
- Preferencias estables
- MCPs realmente reutilizables

### Proyecto
Usa la configuración del proyecto para:

- Stack real
- Comandos reales
- Estructura del repo
- Restricciones locales
- MCPs específicos
- Agentes locales o overrides

### Flujo recomendado
- Project Manager aclara alcance y crea el plan
- Los agentes de implementación trabajan por dominio
- QA Engineer valida comportamiento y regresiones
- SEO & Performance Reviewer revisa superficies públicas si aplica
- Documenter actualiza documentación
- Designer y Marketer participan solo si el proyecto lo necesita

## Casos de uso

### SaaS público

Usar:
- PM
- Frontend
- Backend
- Infra
- QA
- SEO
- Documenter
- Designer
- Marketer

### CRM / dashboard

Usar:
- PM
- Frontend
- Backend
- Infra
- QA
- Documenter

### Microservicio backend

Usar:
- PM
- Backend
- Infra
- QA
- Documenter


## Por qué existe este sistema

Sin estructura, el trabajo multiagente se vuelve ruidoso, inconsistente y difícil de revisar. Este sistema busca convertir Codex CLI en un equipo técnico coordinado, con especialización, límites claros y patrones repetibles.

## Estado

Este repositorio es una base operativa. Debe evolucionar con tus herramientas, skills, MCPs y tipos de proyecto.