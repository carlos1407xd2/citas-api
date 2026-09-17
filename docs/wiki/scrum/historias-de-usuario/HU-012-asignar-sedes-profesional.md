---
id: HU-012
tipo: historia-de-usuario
titulo: Asignar sedes a profesional
estado: Borrador
epica: "[[EP-002-catalogos-y-profesionales]]"
esfuerzo: Medio
sprint_sugerido: "Incremento 2 — Oferta configurable"
dependencias: ["[[HU-001-catalogos-fijos]]", "[[HU-010-crear-y-activar-profesionales]]"]
relacionadas: ["[[HU-013-crear-bloques-disponibilidad]]"]
---
# HU-012 — Asignar sedes a profesional
## Historia de usuario
**COMO** ADMIN **QUIERO** asignar HIC, ICV o ambas sedes al profesional **PARA** limitar dónde puede publicar agenda y atender.
## Alcance
- Relación N:M profesional-sede fija.
## Fuera de alcance
- Crear nuevas sedes.
## Reglas de negocio
- Profesional solo publica en sedes asignadas.
## Dependencias y relaciones
- Épica: [[EP-002-catalogos-y-profesionales]]; depende de [[HU-001-catalogos-fijos]], [[HU-010-crear-y-activar-profesionales]]; relacionada: [[HU-013-crear-bloques-disponibilidad]].
## Esfuerzo
**Nivel:** Medio. **Justificación:** relación N:M y regla de publicación.
## Tareas de desarrollo
- [ ] **T-01 — Modelar asignación de sede.** Dificultad: Medio. Tabla puente/FK.
- [ ] **T-02 — Gestionar asignación ADMIN.** Dificultad: Medio. API/UI y autorización.
- [ ] **T-03 — Probar restricción de agenda.** Dificultad: Medio. Sede asignada/no asignada.
## Criterios de aceptación
### CA-01 — Una o ambas sedes
**Dado** ADMIN y profesional, **cuando** asigna una o ambas sedes fijas, **entonces** las relaciones quedan persistidas.
### CA-02 — Restricción posterior
**Dado** profesional sin asignación a una sede, **cuando** intenta publicar bloque allí, **entonces** se rechaza.
## Definition of Done
- [ ] CA-01 y CA-02 validados.
- [ ] Relación N:M/migración y prueba de restricción evidenciadas.
- [ ] Contrato/UI y trazabilidad Scrum actualizados.
## Evidencia de validación
| Elemento | Resultado | Evidencia | Observación |
|---|---|---|---|
| CA-01 | Pendiente | — | — |
| CA-02 | Pendiente | — | — |
| DoD | Pendiente | — | — |
## Historial de validación
- 2026-09-17 — Creada en `Borrador`.
