---
id: HU-025
tipo: historia-de-usuario
titulo: Consultar agenda profesional
estado: Borrador
epica: "[[EP-006-atencion-y-auditoria]]"
esfuerzo: Medio
sprint_sugerido: "Incremento 7 — Atención trazable"
dependencias: ["[[HU-017-reservar-cita-general]]", "[[HU-019-decidir-cita-especializada]]"]
relacionadas: ["[[HU-026-cerrar-atencion]]"]
---
# HU-025 — Consultar agenda profesional
## Historia de usuario
**COMO** PROFESSIONAL **QUIERO** consultar mis citas `APPROVED` por día/semana y sede **PARA** preparar mi atención sin acceder a información ajena.
## Alcance
- Agenda propia de aprobadas con filtros de día/semana/sede.
## Fuera de alcance
- Citas de otros profesionales o datos de usuarios fuera de las propias citas.
## Reglas de negocio
- Ownership profesional y minimización de datos según RF-16.
## Dependencias y relaciones
- Épica: [[EP-006-atencion-y-auditoria]]; depende de [[HU-017-reservar-cita-general]], [[HU-019-decidir-cita-especializada]]; relacionada: [[HU-026-cerrar-atencion]].
## Esfuerzo
**Nivel:** Medio. **Justificación:** filtros, ownership y proyección de datos.
## Tareas de desarrollo
- [ ] **T-01 — Definir consulta de agenda propia.** Dificultad: Medio. Filtros/índices/ownership.
- [ ] **T-02 — Crear vista de agenda.** Dificultad: Medio. Día, semana, sede y estados UX.
- [ ] **T-03 — Probar privacidad.** Dificultad: Medio. Solo citas propias aprobadas.
## Criterios de aceptación
### CA-01 — Agenda filtrable
**Dado** PROFESSIONAL, **cuando** filtra por día, semana o sede, **entonces** ve sus citas `APPROVED` coincidentes.
### CA-02 — Privacidad
**Dado** citas de otro profesional, **cuando** consulta agenda, **entonces** no puede verlas ni sus datos de usuario.
## Definition of Done
- [ ] CA-01 y CA-02 validados.
- [ ] Ownership, proyección mínima, filtros y pruebas evidenciados.
- [ ] UI/API/documentación Scrum actualizadas.
## Evidencia de validación
| Elemento | Resultado | Evidencia | Observación |
|---|---|---|---|
| CA-01 | Pendiente | — | — |
| CA-02 | Pendiente | — | — |
| DoD | Pendiente | — | — |
## Historial de validación
- 2026-09-17 — Creada en `Borrador`.

