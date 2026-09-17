---
id: HU-026
tipo: historia-de-usuario
titulo: Cerrar atención
estado: Borrador
epica: "[[EP-006-atencion-y-auditoria]]"
esfuerzo: Alto
sprint_sugerido: "Incremento 7 — Atención trazable"
dependencias: ["[[HU-025-consultar-agenda-profesional]]"]
relacionadas: ["[[HU-027-consultar-auditoria-estados]]"]
---
# HU-026 — Cerrar atención
## Historia de usuario
**COMO** PROFESSIONAL **QUIERO** marcar una cita aplicable como `COMPLETED` o `NO_SHOW` **PARA** reflejar el desenlace de la atención.
## Alcance
- Transiciones desde cita propia aprobada aplicable y auditoría.
## Fuera de alcance
- Registrar diagnóstico, tratamiento o historia clínica.
## Reglas de negocio
- RN-11/RN-12; estados explícitos, actor/fuente/fecha registrados.
## Dependencias y relaciones
- Épica: [[EP-006-atencion-y-auditoria]]; depende de [[HU-025-consultar-agenda-profesional]]; relacionada: [[HU-027-consultar-auditoria-estados]].
## Esfuerzo
**Nivel:** Alto. **Justificación:** transiciones, fecha aplicable, ownership e historial inmutable.
## Tareas de desarrollo
- [ ] **T-01 — Validar elegibilidad de cierre.** Dificultad: Alto. Estado/fecha/propiedad.
- [ ] **T-02 — Registrar transición auditable.** Dificultad: Alto. Dominio, persistencia e historial.
- [ ] **T-03 — Integrar acción y pruebas.** Dificultad: Medio. UI/API y casos inválidos.
## Criterios de aceptación
### CA-01 — Cierre válido
**Dado** PROFESSIONAL dueño de cita `APPROVED` pasada/aplicable, **cuando** marca `COMPLETED` o `NO_SHOW`, **entonces** se guarda el nuevo estado.
### CA-02 — Historial
**Dado** cierre realizado, **cuando** se consulta auditoría, **entonces** constan cita, estado, actor, fuente y fecha/hora.
### CA-03 — Protección
**Dado** cita ajena o no aplicable, **cuando** se intenta cerrar, **entonces** se rechaza.
## Definition of Done
- [ ] CA-01 a CA-03 validados.
- [ ] Máquina de estados, ownership e historial inmutable evidenciados.
- [ ] UI/API y pruebas relevantes actualizadas.
## Evidencia de validación
| Elemento | Resultado | Evidencia | Observación |
|---|---|---|---|
| CA-01 | Pendiente | — | — |
| CA-02 | Pendiente | — | — |
| CA-03 | Pendiente | — | — |
| DoD | Pendiente | — | — |
## Historial de validación
- 2026-09-17 — Creada en `Borrador`.

