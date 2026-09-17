---
id: HU-017
tipo: historia-de-usuario
titulo: Reservar cita general
estado: Borrador
epica: "[[EP-004-reserva-y-ciclo-de-cita]]"
esfuerzo: Alto
sprint_sugerido: "Incremento 4 — Cita general"
dependencias: ["[[HU-016-consultar-disponibilidad]]"]
relacionadas: ["[[HU-021-consultar-mis-citas]]", "[[HU-027-consultar-auditoria-estados]]"]
---
# HU-017 — Reservar cita general
## Historia de usuario
**COMO** USER **QUIERO** confirmar una cita de Medicina General en un horario disponible **PARA** obtener atención sin aprobación administrativa.
## Alcance
- Selección de profesional general/franja y creación APPROVED.
## Fuera de alcance
- Cita especializada.
## Reglas de negocio
- RN-01 y RN-02; validar disponibilidad al confirmar.
## Dependencias y relaciones
- Épica: [[EP-004-reserva-y-ciclo-de-cita]]; depende de [[HU-016-consultar-disponibilidad]]; relacionadas: [[HU-021-consultar-mis-citas]], [[HU-027-consultar-auditoria-estados]].
## Esfuerzo
**Nivel:** Alto. **Justificación:** reserva transaccional, estado automático, historial y UI.
## Tareas de desarrollo
- [ ] **T-01 — Modelar cita/reserva/historial.** Dificultad: Alto. Flyway 3FN, FKs e índices.
- [ ] **T-02 — Confirmar con control de doble reserva.** Dificultad: Alto. Transacción/constraint y validación final.
- [ ] **T-03 — Integrar confirmación y prueba concurrente.** Dificultad: Alto. UI y pruebas API.
## Criterios de aceptación
### CA-01 — Aprobación automática
**Dado** USER, Medicina General y franja aún disponible, **cuando** confirma, **entonces** se crea cita `APPROVED`.
### CA-02 — Sin doble reserva
**Dado** franja tomada entre consulta y confirmación, **cuando** USER confirma, **entonces** se rechaza y no se crea cita duplicada.
### CA-03 — Auditoría
**Dado** cita general creada, **cuando** se revisa historial, **entonces** existe transición auditable con fuente/actor aplicables.
## Definition of Done
- [ ] CA-01 a CA-03 validados, incluyendo prueba de contención/concurrencia aplicable.
- [ ] Migración, integridad de slots, estado e historial evidenciados.
- [ ] Confirmación UI/API y contrato REST actualizados.
## Evidencia de validación
| Elemento | Resultado | Evidencia | Observación |
|---|---|---|---|
| CA-01 | Pendiente | — | — |
| CA-02 | Pendiente | — | — |
| CA-03 | Pendiente | — | — |
| DoD | Pendiente | — | — |
## Historial de validación
- 2026-09-17 — Creada en `Borrador`.

