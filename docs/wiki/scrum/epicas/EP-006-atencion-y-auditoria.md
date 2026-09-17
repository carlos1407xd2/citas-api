---
id: EP-006
tipo: epica
titulo: Atención y auditoría
estado: Borrador
historias: ["[[HU-025-consultar-agenda-profesional]]", "[[HU-026-cerrar-atencion]]", "[[HU-027-consultar-auditoria-estados]]"]
dependencias: ["[[EP-004-reserva-y-ciclo-de-cita]]", "[[EP-005-gestion-administrativa]]"]
---
# EP-006 — Atención y auditoría
## Objetivo
Permitir la atención profesional y trazabilidad inmutable de estados.
## Valor esperado
Agenda con privacidad y evidencia de cada transición.
## Actores
- PROFESSIONAL
- ADMIN
## Alcance
- Agenda propia, COMPLETED/NO_SHOW e historial.
## Fuera de alcance
- Historia clínica.
## Reglas de negocio
- Solo propias citas visibles al profesional; auditoría no es CRUD normal.
## Dependencias
- [[EP-004-reserva-y-ciclo-de-cita]], [[EP-005-gestion-administrativa]]
## Historias de usuario
- [[HU-025-consultar-agenda-profesional]]
- [[HU-026-cerrar-atencion]]
- [[HU-027-consultar-auditoria-estados]]
## Criterio de completitud de la épica
- [ ] Cierre y auditoría mantienen actor, fuente, fecha y motivo aplicable.
## Riesgos e incógnitas
- Definir qué actores pueden consultar el historial sin exponer datos fuera de ownership.
