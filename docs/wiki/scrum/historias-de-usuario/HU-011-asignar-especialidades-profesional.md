---
id: HU-011
tipo: historia-de-usuario
titulo: Asignar especialidades a profesional
estado: Borrador
epica: "[[EP-002-catalogos-y-profesionales]]"
esfuerzo: Alto
sprint_sugerido: "Incremento 2 — Oferta configurable"
dependencias: ["[[HU-009-gestionar-especialidades]]", "[[HU-010-crear-y-activar-profesionales]]"]
relacionadas: ["[[HU-016-consultar-disponibilidad]]"]
---
# HU-011 — Asignar especialidades a profesional
## Historia de usuario
**COMO** ADMIN **QUIERO** asignar una o varias especialidades y una primaria al profesional **PARA** definir qué servicios puede atender.
## Alcance
- Relación N:M profesional-especialidad y marca primaria.
## Fuera de alcance
- Duración editable por profesional.
## Reglas de negocio
- Especialidad debe estar activa; la primaria pertenece al conjunto asignado.
## Dependencias y relaciones
- Épica: [[EP-002-catalogos-y-profesionales]]; depende de [[HU-009-gestionar-especialidades]], [[HU-010-crear-y-activar-profesionales]]; relacionada: [[HU-016-consultar-disponibilidad]].
## Esfuerzo
**Nivel:** Alto. **Justificación:** N:M, integridad de primaria y reserva dependiente.
## Tareas de desarrollo
- [ ] **T-01 — Modelar relación puente 3FN.** Dificultad: Alto. Únicos y regla de primaria.
- [ ] **T-02 — Gestionar asignaciones ADMIN.** Dificultad: Medio. API/UI protegida.
- [ ] **T-03 — Probar elegibilidad de reserva.** Dificultad: Alto. Activa/asignada/primaria.
## Criterios de aceptación
### CA-01 — Asignación múltiple
**Dado** ADMIN, profesional y especialidades activas, **cuando** asigna varias, **entonces** quedan asociadas sin listas desnormalizadas.
### CA-02 — Primaria válida
**Dado** especialidades asignadas, **cuando** marca una primaria, **entonces** pertenece al profesional y se identifica como tal.
### CA-03 — Especialidad no disponible
**Dado** especialidad no activa o no asignada, **cuando** se intenta usar para ese profesional, **entonces** no se ofrece ni reserva.
## Definition of Done
- [ ] CA-01 a CA-03 validados.
- [ ] Tabla puente/migración, constraints y pruebas de elegibilidad evidenciados.
- [ ] Contrato/UI y wikilinks actualizados.
## Evidencia de validación
| Elemento | Resultado | Evidencia | Observación |
|---|---|---|---|
| CA-01 | Pendiente | — | — |
| CA-02 | Pendiente | — | — |
| CA-03 | Pendiente | — | — |
| DoD | Pendiente | — | — |
## Historial de validación
- 2026-09-17 — Creada en `Borrador`.

