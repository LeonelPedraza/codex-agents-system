# Guía de instalación

Esta guía explica cómo instalar y organizar el sistema de agentes de Codex CLI en tu máquina y cómo usar la plantilla de proyecto en nuevos repositorios.

## Objetivo

Montar un entorno reutilizable con:

- guía global en `AGENTS.md`
- configuración global
- subagentes personalizados globales
- skills opcionales
- plantilla por proyecto

## 1. Crear la estructura global de Codex

Crea esta estructura en tu directorio personal:

```
~/.codex/
├─ AGENTS.md
├─ config.toml
├─ agents/
└─ skills/
```

### Archivos que van ahí
- ~/.codex/AGENTS.md
- ~/.codex/config.toml
- ~/.codex/agents/project_manager.toml
- ~/.codex/agents/frontend_developer.toml
- ~/.codex/agents/backend_developer.toml
- ~/.codex/agents/qa_engineer.toml
- ~/.codex/agents/seo_performance_reviewer.toml
- ~/.codex/agents/infra_devops.toml
- ~/.codex/agents/documenter.toml
- ~/.codex/agents/designer.toml
- ~/.codex/agents/marketer.toml

## 2. Revisar herramientas y conectores

El sistema está pensado para trabajar con herramientas como:

### Core
- shell_command
- web
- chrome_devtools
- playwright
- Conectores / apps
- Canva
- Figma
- GitHub
- Gmail
- Google Calendar
- Notion
- Vercel

### Integraciones adicionales
- Redis
- Stitch
- InVideo
- Manus
- Lovable
- Namecheap

Activa globalmente solo lo que usas en muchos proyectos. Lo específico de un repositorio debe quedarse en la configuración local del proyecto.

## 3. Preparar la configuración global

Tu ```~/.codex/config.toml``` debería definir:

- modelo por defecto
- esfuerzo de razonamiento
- sandbox
- approval policy
- concurrencia de agentes
- MCPs globales reutilizables

La idea es que la configuración global sea estable, pequeña y reutilizable.

## 4. Copiar la plantilla en cada nuevo proyecto

Para cada repositorio nuevo, copia esta estructura:

```
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

Luego rellena:
- stack
- comandos
- carpetas
- restricciones
- agentes activos
- MCPs específicos del proyecto

## 5. Flujo recomendado al iniciar un proyecto
1. copiar la plantilla
2. completar AGENTS.md
3. completar .codex/config.toml
4. crear los primeros documentos en docs/
5. usar project_manager para aclarar alcance
6. dividir el trabajo por especialistas
7. validar y documentar antes de cerrar

## 6. Reglas operativas recomendadas
- No dejar que varios agentes editen los mismos archivos al mismo tiempo
- Planificar primero cuando el trabajo sea ambiguo o grande
- Preferir cambios pequeños y revisables
- Mantener lo global genérico
- Mantener lo local concreto
- Usar skills para workflows repetibles
- Tratar la documentación como un artefacto real del proyecto

## 7. Primera prueba recomendada

### Haz una primera prueba así:

1. Abre un repositorio nuevo o existente
2. Añade la plantilla del proyecto
3. Pide a project_manager que:
   - Aclare el proyecto
   - Resuma objetivos
   - Defina flujos
   - Identifique entidades clave
   - Proponga workstreams
4. Después delega a:
   - backend
   - frontend
   - infra
   - QA
   - documenter

## 8. Mantenimiento

Revisa este sistema periódicamente:
- Elimina agentes que no uses de verdad
- Ajusta scopes si hay demasiado solapamiento
- Añade agentes locales solo cuando estén justificados
- Mantén la documentación corta, práctica y actual