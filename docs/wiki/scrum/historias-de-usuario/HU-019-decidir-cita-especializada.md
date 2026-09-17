---
id: HU-019
tipo: historia-de-usuario
titulo: Decidir cita especializada
estado: Borrador
epica: "[[EP-005-gestion-administrativa]]"
esfuerzo: Alto
sprint_sugerido: "Incremento 5 — Cita especializada"
dependencias: ["[[HU-018-solicitar-cita-especializada]]"]
relacionadas: ["[[HU-027-consultar-auditoria-estados]]"]
---
# HU-019 — Decidir cita especializada
## Historia de usuario
**COMO** ADMIN **QUIERO** aprobar o rechazar una solicitud especializada **PARA** controlar la asignación de atención.
## Alcance
- Decisión de cita `REQUESTED`, motivo obligatorio de rechazo y ajuste de slots.
## Fuera de alcance
- Decisión de cita general.
## Reglas de negocio
- Aprobada pasa a `APPROVED`; rechazada a `REJECTED` y libera slots; rechazo exige motivo.
## Dependencias y relaciones
- Épica: [[EP-005-gestion-administrativa]]; depende de [[HU-018-solicitar-cita-especializada]]; relacionada: [[HU-027-consultar-auditoria-estados]].
## Esfuerzo
**Nivel:** Alto. **Justificación:** transición autorizada, reserva e historial.
## Tareas de desarrollo
- [ ] **T-01 — Aplicar máquina de estados.** Dificultad: Alto. Validación `REQUESTED` y motivo.
- [ ] **T-02 — Ajustar reservas/historial atómicamente.** Dificultad: Alto. Persistencia/transaction.
- [ ] **T-03 — Integrar decisión ADMIN y pruebas.** Dificultad: Alto. UI/API/autorización.
## Criterios de aceptación
### CA-01 — Aprobación
**Dado** solicitud `REQUESTED`, **cuando** ADMIN aprueba, **entonces** queda `APPROVED` y mantiene su reserva.
### CA-02 — Rechazo motivado
**Dado** solicitud `REQUESTED`, **cuando** ADMIN rechaza con motivo, **entonces** queda `REJECTED`, conserva el motivo y libera slots.
### CA-03 — Transición protegida
**Dado** actor no ADMIN o solicitud ya decidida, **cuando** intenta decidir, **entonces** se rechaza sin alterar estado/reserva.
## Definition of Done
- [ ] CA-01 a CA-03 validados.
- [ ] Transiciones, motivo, liberación e historial auditables.
- [ ] UI/API, autorización y pruebas relevantes evidenciadas.
## Evidencia de validación
| Elemento | Resultado | Evidencia | Observación |
|---|---|---|---|
| CA-01 | Pendiente | — | — |
| CA-02 | Pendiente | — | — |
| CA-03 | Pendiente | — | — |
| DoD | Pendiente | — | — |
## Historial de validación
- 2026-09-17 — Creada en `Borrador`.

