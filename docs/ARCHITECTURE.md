# Arquitectura del sistema

## Visión general

Este repositorio define un modelo de trabajo por capas para Codex CLI, separando el comportamiento global reutilizable de la especialización por proyecto.

Está diseñado para soportar:

- trabajo en paralelo
- subagentes especializados
- flujos reutilizables de planificación y entrega
- múltiples repositorios
- estándares de ingeniería consistentes

## Capas

### Capa 1: guía global en AGENTS
Ubicación:
- `~/.codex/AGENTS.md`

Propósito:
- definir el modelo universal de trabajo
- establecer reglas de colaboración
- definir el contrato de salida
- definir la política de planificación
- definir expectativas de validación

Esta capa debe ser estable entre proyectos.

### Capa 2: configuración global del CLI
Ubicación:
- `~/.codex/config.toml`

Propósito:
- definir modelo y razonamiento por defecto
- definir sandbox y approvals
- controlar concurrencia y profundidad
- configurar MCPs ampliamente reutilizables

Esta capa debe ser pequeña y estable.

### Capa 3: subagentes globales personalizados
Ubicación:
- `~/.codex/agents/*.toml`

Propósito:
- definir agentes reutilizables
- acotar responsabilidades
- limitar superficie de herramientas y skills
- asegurar colaboración repetible

Esta es la biblioteca global de agentes.

### Capa 4: plantilla de proyecto y overrides locales
Ubicación:
- `<repo>/AGENTS.md`
- `<repo>/.codex/config.toml`
- `<repo>/.codex/agents/*.toml` cuando sea necesario

Propósito:
- adaptar el sistema global al repositorio
- definir stack, estructura, comandos y restricciones
- configurar integraciones del proyecto
- definir comportamiento específico del dominio

## Modelo de orquestación

El flujo recomendado es:

1. `project_manager`
2. agentes especialistas
3. `qa_engineer`
4. `documenter`

Revisiones opcionales:
- `seo_performance_reviewer`
- `designer`
- `marketer`

## Ciclo recomendado de trabajo

### Planificación
`project_manager`:
- aclara requisitos
- identifica stakeholders
- define flujos
- crea arquitectura y desglose de tareas
- separa workstreams

### Implementación
Los especialistas trabajan por dominio:
- frontend
- backend
- infra

Cada uno debe operar con alcance acotado y mínima superposición.

### Validación
`qa_engineer` verifica:
- comportamiento
- regresiones
- huecos de cobertura
- reproducibilidad

### Documentación
`documenter` actualiza:
- requirements
- architecture
- test plan
- release notes
- readme o runbooks si aplica

## Por qué no dejar todo global

Una configuración totalmente global se vuelve demasiado genérica y ruidosa. Cada repositorio necesita instrucciones locales para:
- comandos reales
- stack concreto
- estructura de carpetas
- reglas de despliegue
- restricciones del dominio

## Por qué no dejar todo por proyecto

Eso duplicaría demasiado:
- roles
- colaboración
- contrato de salida
- estilo de trabajo

Por eso el sistema es intencionalmente híbrido.

## Restricciones de diseño

- los agentes deben ser estrechos y opinados
- las skills deben manejar workflows reutilizables
- la documentación debe reflejar el estado real del proyecto
- las instrucciones específicas deben vivir cerca del repositorio
- los defaults globales deben mantenerse reutilizables