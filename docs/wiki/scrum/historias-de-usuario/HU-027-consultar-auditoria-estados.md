---
id: HU-027
tipo: historia-de-usuario
titulo: Consultar auditoría de estados
estado: Borrador
epica: "[[EP-006-atencion-y-auditoria]]"
esfuerzo: Medio
sprint_sugerido: "Incremento 7 — Atención trazable"
dependencias: ["[[HU-017-reservar-cita-general]]", "[[HU-019-decidir-cita-especializada]]", "[[HU-022-cancelar-cita]]", "[[HU-024-decidir-reprogramacion]]", "[[HU-026-cerrar-atencion]]"]
relacionadas: []
---
# HU-027 — Consultar auditoría de estados
## Historia de usuario
**COMO** actor autorizado según ownership o rol **QUIERO** consultar el historial de estados de una cita **PARA** conocer trazablemente sus cambios.
## Alcance
- Historial de cita: estado nuevo, actor cuando exista, fuente SYSTEM/USER/ADMIN, fecha/hora y motivo opcional.
## Fuera de alcance
- CRUD normal o alteración de registros de auditoría.
## Reglas de negocio
- RN-12; se preserva integridad y acceso autorizado.
## Dependencias y relaciones
- Épica: [[EP-006-atencion-y-auditoria]]; depende de [[HU-017-reservar-cita-general]], [[HU-019-decidir-cita-especializada]], [[HU-022-cancelar-cita]], [[HU-024-decidir-reprogramacion]], [[HU-026-cerrar-atencion]].
## Esfuerzo
**Nivel:** Medio. **Justificación:** historial inmutable, autorización y proyección segura.
## Tareas de desarrollo
- [ ] **T-01 — Modelar/consultar historial inmutable.** Dificultad: Medio. FK, índices y proyección.
- [ ] **T-02 — Aplicar autorización de consulta.** Dificultad: Alto. Ownership/rol definido por contrato aprobado.
- [ ] **T-03 — Probar completitud y no edición.** Dificultad: Medio. Transiciones y protección.
## Criterios de aceptación
### CA-01 — Contenido trazable
**Dado** cita con cambios, **cuando** actor autorizado consulta historial, **entonces** ve estado, actor aplicable, fuente, fecha/hora y motivo si existe.
### CA-02 — Inmutabilidad
**Dado** registro de historial, **cuando** se intenta editarlo mediante flujo CRUD, **entonces** la operación no está disponible.
### CA-03 — Acceso protegido
**Dado** actor no autorizado, **cuando** intenta consultar auditoría de una cita ajena, **entonces** se rechaza.
## Definition of Done
- [ ] CA-01 a CA-03 validados.
- [ ] Inmutabilidad, autorización e índices/relaciones 3FN evidenciados.
- [ ] Contrato de visibilidad y trazabilidad Scrum actualizados.
## Evidencia de validación
| Elemento | Resultado | Evidencia | Observación |
|---|---|---|---|
| CA-01 | Pendiente | — | — |
| CA-02 | Pendiente | — | — |
| CA-03 | Pendiente | — | — |
| DoD | Pendiente | — | — |
## Historial de validación
- 2026-09-17 — Creada en `Borrador`.

