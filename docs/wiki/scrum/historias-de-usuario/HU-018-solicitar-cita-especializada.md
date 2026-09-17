---
id: HU-018
tipo: historia-de-usuario
titulo: Solicitar cita especializada
estado: Borrador
epica: "[[EP-004-reserva-y-ciclo-de-cita]]"
esfuerzo: Alto
sprint_sugerido: "Incremento 5 — Cita especializada"
dependencias: ["[[HU-016-consultar-disponibilidad]]"]
relacionadas: ["[[HU-019-decidir-cita-especializada]]", "[[HU-020-consultar-bandeja-administrativa]]"]
---
# HU-018 — Solicitar cita especializada
## Historia de usuario
**COMO** USER **QUIERO** solicitar una cita especializada con sede, profesional y horario **PARA** que ADMIN evalúe mi solicitud sin perder la franja.
## Alcance
- Crear solicitud `REQUESTED` y retener slots.
## Fuera de alcance
- Decisión ADMIN.
## Reglas de negocio
- RN-01 y RN-03; especialidad activa/asignada y horario disponible al confirmar.
## Dependencias y relaciones
- Épica: [[EP-004-reserva-y-ciclo-de-cita]]; depende de [[HU-016-consultar-disponibilidad]]; relacionadas: [[HU-019-decidir-cita-especializada]], [[HU-020-consultar-bandeja-administrativa]].
## Esfuerzo
**Nivel:** Alto. **Justificación:** retención consistente, estado y flujo cross-role.
## Tareas de desarrollo
- [ ] **T-01 — Crear solicitud/reserva retenida.** Dificultad: Alto. Modelo/estado/migración.
- [ ] **T-02 — Confirmar disponibilidad atómicamente.** Dificultad: Alto. Antidoble reserva.
- [ ] **T-03 — Integrar formulario y pruebas.** Dificultad: Alto. UI, API, historial.
## Criterios de aceptación
### CA-01 — Solicitud retenida
**Dado** selección especializada válida y franja libre, **cuando** USER confirma, **entonces** nace cita `REQUESTED` y sus slots quedan retenidos.
### CA-02 — Sin colisión
**Dado** franja no disponible al confirmar, **cuando** USER solicita, **entonces** no se crea ni retiene una segunda reserva.
### CA-03 — Visible a administración
**Dado** solicitud creada, **cuando** ADMIN consulta la bandeja, **entonces** puede identificarla para decisión.
## Definition of Done
- [ ] CA-01 a CA-03 validados.
- [ ] Retención, estado, migración/historial y prueba de integridad evidenciados.
- [ ] Formulario, contrato y trazabilidad actualizados.
## Evidencia de validación
| Elemento | Resultado | Evidencia | Observación |
|---|---|---|---|
| CA-01 | Pendiente | — | — |
| CA-02 | Pendiente | — | — |
| CA-03 | Pendiente | — | — |
| DoD | Pendiente | — | — |
## Historial de validación
- 2026-09-17 — Creada en `Borrador`.
