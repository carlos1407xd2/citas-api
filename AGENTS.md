# `citas-api` — instrucciones para agentes

## Estado comprobado del repositorio

Este repositorio todavía no contiene una aplicación Spring Boot: no hay `pom.xml`, código Java, pruebas ni migraciones. Actualmente contiene la documentación compartida, especificaciones Markdown de automatización y la LLM Wiki global. No asumir nombres de paquetes, módulos, perfiles, endpoints ni estructura de directorios hasta que el proyecto real exista.

La rama de trabajo es `develop`; `main` representa puntos estables. No reescribir historial ni borrar evidencia de progreso.

## Fuentes obligatorias

Antes de modificar backend, leer `../PRD.md`, `../RESTRICCIONES_TECNICAS.md`, `../database/REQUISITOS_NORMALIZACION_3FN.md`, `README.md` y el índice de la wiki global en `docs/wiki/llm-wiki/wiki/index.md`.

Una HU aprobada con criterios de aceptación y DoD es requisito previo para implementar funcionalidad. Si no existe, informar el bloqueo al orquestador; no derivar una HU implícita del PRD.

## Responsabilidad backend

Implementar exclusivamente en este repositorio Java 21, Spring Boot 3.5.x, Maven, REST/JSON, MySQL 8.4, Spring Data JPA, Flyway, Spring Security y JWT access/refresh, conforme al PRD y restricciones aprobadas.

El dominio no depende de Spring, JPA ni HTTP. Los casos de uso pertenecen a aplicación; los puertos definen las dependencias; REST y persistencia son adaptadores. Los controladores traducen HTTP y no concentran reglas de negocio. No acoplar el backend a React o Angular ni editar `../citas-web`.

## Reglas no negociables

- Mantener en backend la autoridad de validación, autorización, ownership, estados, reservas y reglas de agenda.
- No permitir doble reserva, ni bloques/citas en el pasado, ni reservas de especialidades inactivas o no asignadas al profesional.
- Usar hashes adaptativos para contraseñas; separar access y refresh tokens; no registrar passwords ni tokens.
- Usar únicamente variables de entorno para secretos; nunca abrir, copiar ni publicar `.env`.
- Cada modificación de esquema debe incluir una migración Flyway versionada, justificación de normalización 3FN e índices/constraints pertinentes.
- Catálogos referenciados por transacciones se desactivan cuando aplique; no se borran físicamente.
- Usar datos sintéticos. No incorporar datos privados reales de FCV.

## Flujo de trabajo

1. Localizar la HU, CA y DoD aprobados.
2. Identificar reglas del PRD, puertos/adaptadores, persistencia, seguridad y contrato REST afectados.
3. Proponer el plan, incluyendo archivos a modificar y migraciones si aplica.
4. Implementar el incremento mínimo coherente.
5. Ejecutar las pruebas disponibles: dominio, aplicación e integración REST/persistencia relevantes. Si aún no hay build configurado, declararlo explícitamente.
6. Verificar que el dominio siga independiente de los adaptadores y que el DoD se cumpla.
7. Resumir evidencia, riesgos y aspectos no verificados.

Un cambio de contrato REST debe escalarse al orquestador para coordinación y evidencia en ambos repositorios. No mantener ni modificar una wiki propia: `docs/wiki/llm-wiki/` es global y la mantiene el orquestador. La Skill `scrum-spec-orchestrator` es la única que escribe en `docs/wiki/scrum/` y nunca implementa código.

## Automatizaciones

Los archivos actuales de `automations/n8n/` son especificaciones, no workflows implementados. En S5/S6, los workflows se exportan como JSON en esa ruta sin secretos ni credenciales embebidas.
