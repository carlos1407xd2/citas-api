---
id: HU-022
tipo: historia-de-usuario
titulo: Cancelar cita
estado: Borrador
epica: "[[EP-004-reserva-y-ciclo-de-cita]]"
esfuerzo: Alto
sprint_sugerido: "Incremento 6 — Ciclo del usuario"
dependencias: ["[[HU-021-consultar-mis-citas]]"]
relacionadas: ["[[HU-027-consultar-auditoria-estados]]"]
---
# HU-022 — Cancelar cita
## Historia de usuario
**COMO** USER **QUIERO** cancelar una cita futura no terminal **PARA** liberar el horario que ya no usaré.
## Alcance
- Transición a `CANCELLED`, liberación de slots e historial.
## Fuera de alcance
- Reactivar una cancelada.
## Reglas de negocio
- Solo propia, futura y no terminal; RN-09 y RN-11.
## Dependencias y relaciones
- Épica: [[EP-004-reserva-y-ciclo-de-cita]]; depende de [[HU-021-consultar-mis-citas]]; relacionada: [[HU-027-consultar-auditoria-estados]].
## Esfuerzo
**Nivel:** Alto. **Justificación:** estado, slots, ownership e historial.
## Tareas de desarrollo
- [ ] **T-01 — Validar transición cancelable.** Dificultad: Alto. Dominio/ownership/fecha.
- [ ] **T-02 — Liberar reserva y registrar historial.** Dificultad: Alto. Transacción.
- [ ] **T-03 — Integrar acción y pruebas.** Dificultad: Medio. UI/API y casos terminales.
## Criterios de aceptación
### CA-01 — Cancelación válida
**Dado** cita propia futura no terminal, **cuando** USER cancela, **entonces** queda `CANCELLED` y libera sus slots.
### CA-02 — No reactivación
**Dado** cita `CANCELLED`, **cuando** se intenta reactivarla directamente, **entonces** se rechaza.
### CA-03 — Restricciones
**Dado** cita ajena, pasada o terminal, **cuando** USER intenta cancelarla, **entonces** no cambia.
## Definition of Done
- [ ] CA-01 a CA-03 validados.
- [ ] Liberación, historial y restricciones de estado evidenciados.
- [ ] UI/API y pruebas aplicables actualizadas.
## Evidencia de validación
| Elemento | Resultado | Evidencia | Observación |
|---|---|---|---|
| CA-01 | Pendiente | — | — |
| CA-02 | Pendiente | — | — |
| CA-03 | Pendiente | — | — |
| DoD | Pendiente | — | — |
## Historial de validación
- 2026-09-17 — Creada en `Borrador`.

