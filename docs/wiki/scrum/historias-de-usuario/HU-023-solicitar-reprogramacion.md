---
id: HU-023
tipo: historia-de-usuario
titulo: Solicitar reprogramación
estado: Borrador
epica: "[[EP-004-reserva-y-ciclo-de-cita]]"
esfuerzo: Alto
sprint_sugerido: "Incremento 6 — Ciclo del usuario"
dependencias: ["[[HU-016-consultar-disponibilidad]]", "[[HU-021-consultar-mis-citas]]"]
relacionadas: ["[[HU-024-decidir-reprogramacion]]"]
---
# HU-023 — Solicitar reprogramación
## Historia de usuario
**COMO** USER **QUIERO** solicitar una nueva fecha/hora para mi cita aprobada futura **PARA** intentar cambiarla sin perder la original mientras se decide.
## Alcance
- Reprogramación `PENDING`, mismo profesional/especialidad, retención nueva.
## Fuera de alcance
- Cambiar profesional; es nueva cita.
## Reglas de negocio
- RN-10; original conserva franja hasta decisión; nueva debe estar disponible.
## Dependencias y relaciones
- Épica: [[EP-004-reserva-y-ciclo-de-cita]]; depende de [[HU-016-consultar-disponibilidad]], [[HU-021-consultar-mis-citas]]; relacionada: [[HU-024-decidir-reprogramacion]].
## Esfuerzo
**Nivel:** Alto. **Justificación:** dos franjas, reserva provisional y estados vinculados.
## Tareas de desarrollo
- [ ] **T-01 — Modelar solicitud y reserva provisional.** Dificultad: Alto. 3FN/FKs/estado.
- [ ] **T-02 — Validar cita original y nueva franja.** Dificultad: Alto. Mismo profesional/especialidad.
- [ ] **T-03 — Crear flujo UI/API y pruebas.** Dificultad: Alto. Original conservada y contención.
## Criterios de aceptación
### CA-01 — Solicitud elegible
**Dado** cita propia `APPROVED` futura, **cuando** USER elige franja disponible del mismo profesional/especialidad, **entonces** se crea reprogramación `PENDING` y nueva franja queda retenida.
### CA-02 — Original preservada
**Dado** reprogramación pendiente, **cuando** se consulta la cita original, **entonces** mantiene su fecha/hora y reserva original.
### CA-03 — Restricciones
**Dado** cita no aprobada/no futura o cambio de profesional, **cuando** USER solicita, **entonces** se rechaza.
## Definition of Done
- [ ] CA-01 a CA-03 validados.
- [ ] Modelo/migración, ambas reservas y reglas de elegibilidad evidenciados.
- [ ] Flujo UI/API y pruebas de integridad actualizados.
## Evidencia de validación
| Elemento | Resultado | Evidencia | Observación |
|---|---|---|---|
| CA-01 | Pendiente | — | — |
| CA-02 | Pendiente | — | — |
| CA-03 | Pendiente | — | — |
| DoD | Pendiente | — | — |
## Historial de validación
- 2026-09-17 — Creada en `Borrador`.

