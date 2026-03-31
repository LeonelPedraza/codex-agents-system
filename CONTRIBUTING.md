# Guía de contribución

Gracias por contribuir a este repositorio.

El objetivo de este proyecto es mantener un sistema claro, reutilizable y bien documentado para trabajar con Codex CLI usando agentes especializados, configuración global y plantillas por proyecto.

## Objetivo de las contribuciones

Las contribuciones deben ayudar a mejorar alguna de estas áreas:

- claridad de la documentación
- calidad del sistema de agentes
- organización de la arquitectura global y por proyecto
- plantillas reutilizables
- ejemplos prácticos
- mantenimiento del repositorio
- compatibilidad con nuevos flujos de trabajo
- mejoras reales en usabilidad

## Tipos de contribuciones aceptadas

Se aceptan contribuciones como:

- correcciones de errores en la documentación
- mejoras de redacción
- reorganización de archivos o estructura del repositorio
- nuevas plantillas por tipo de proyecto
- mejoras en los ejemplos
- ampliación del catálogo de agentes
- mejoras en la separación entre configuración global y local
- mejores prácticas para workflows con Codex CLI

## Tipos de contribuciones que conviene evitar

No se recomienda contribuir con cambios que:

- hagan el sistema más complejo sin una ventaja clara
- dupliquen información ya existente
- añadan agentes innecesarios o demasiado genéricos
- mezclen comportamiento global con detalles específicos de un proyecto
- conviertan la documentación en texto inflado o poco accionable
- introduzcan reglas excesivamente rígidas que no sean reutilizables

## Principios para contribuir

Antes de proponer un cambio, asegúrate de seguir estos principios:

- mantener el sistema simple
- priorizar reutilización
- documentar con claridad
- evitar duplicaciones
- mantener separados los conceptos globales y locales
- favorecer cambios pequeños y revisables
- justificar cambios estructurales importantes

## Flujo recomendado de contribución

### 1. Crear una rama
Crea una rama específica para tu cambio.

Ejemplos:
- `docs/mejora-readme`
- `templates/nueva-plantilla-saas`
- `agents/mejora-catalogo`
- `infra/reorganizacion-repo`

### 2. Hacer cambios acotados
Intenta que cada contribución tenga un objetivo claro y limitado.

### 3. Validar consistencia
Antes de enviar cambios, revisa que:

- no haya archivos duplicados
- no haya contradicciones entre documentos
- la estructura del repositorio siga siendo clara
- el lenguaje usado sea consistente
- los ejemplos sean coherentes con la arquitectura propuesta

### 4. Documentar el cambio
Si el cambio modifica estructura, comportamiento o convenciones, actualiza también:
- `README.md`
- `SETUP.md`
- documentos dentro de `docs/`
- plantillas afectadas

## Convenciones de redacción

Este repositorio prioriza documentación:

- clara
- concreta
- accionable
- sin relleno innecesario
- técnicamente consistente

Intenta escribir de forma:
- directa
- ordenada
- fácil de copiar y aplicar
- evitando ambigüedades

## Convenciones estructurales

Cuando agregues contenido nuevo:

- usa nombres de archivos claros
- mantén la jerarquía del repositorio limpia
- evita crear carpetas innecesarias
- no mezcles ejemplos, plantillas y documentación conceptual en un mismo archivo

## Sobre agentes y plantillas

Si propones cambios al sistema de agentes:

- explica por qué el cambio mejora el flujo
- indica si es un cambio global o por proyecto
- evita crear agentes que solapen demasiado responsabilidades
- intenta mantener los agentes estrechos y especializados

Si propones nuevas plantillas:

- indica el tipo de proyecto al que aplican
- deja claro qué partes son reutilizables
- mantén las plantillas simples y editables

## Sobre ejemplos

Si agregas ejemplos, intenta que sean:

- realistas
- pequeños
- bien organizados
- fáciles de adaptar
- alineados con la arquitectura descrita en este repositorio

## Pull requests

Al abrir un pull request, incluye:

1. qué problema resuelve
2. qué archivos cambiaste
3. por qué el cambio es útil
4. si afecta documentación, plantillas o arquitectura
5. si requiere actualizar otros archivos relacionados

## Checklist antes de contribuir

Antes de abrir tu contribución, revisa esto:

- [ ] el cambio tiene un objetivo claro
- [ ] no rompe la estructura del repositorio
- [ ] la documentación sigue siendo consistente
- [ ] actualicé archivos relacionados si era necesario
- [ ] no añadí complejidad innecesaria
- [ ] el contenido sigue siendo claro y reutilizable

## Filosofía general

Este repositorio no busca acumular contenido. Busca construir un sistema de trabajo útil, mantenible y fácil de replicar.

Contribuye con cambios que realmente hagan mejor el sistema.