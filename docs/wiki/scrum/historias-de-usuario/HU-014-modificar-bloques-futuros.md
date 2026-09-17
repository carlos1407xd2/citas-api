---
id: HU-014
tipo: historia-de-usuario
titulo: Modificar bloques futuros
estado: Borrador
epica: "[[EP-003-disponibilidad-profesional]]"
esfuerzo: Alto
sprint_sugerido: "Incremento 3 — Agenda publicable"
dependencias: ["[[HU-013-crear-bloques-disponibilidad]]"]
relacionadas: ["[[HU-015-consultar-calendario-profesional]]"]
---
# HU-014 — Modificar bloques futuros
## Historia de usuario
**COMO** PROFESSIONAL **QUIERO** editar o eliminar mis bloques futuros sin citas comprometidas **PARA** mantener mi agenda disponible al día.
## Alcance
- Edición/eliminación propia de bloques futuros sin cita comprometida.
## Fuera de alcance
- Alterar bloques pasados o slots reservados/retenidos.
## Reglas de negocio
- No se elimina/edita bloque con citas comprometidas; ownership obligatorio.
## Dependencias y relaciones
- Épica: [[EP-003-disponibilidad-profesional]]; depende de [[HU-013-crear-bloques-disponibilidad]]; relacionada: [[HU-015-consultar-calendario-profesional]].
## Esfuerzo
**Nivel:** Alto. **Justificación:** preservación de reservas y validación temporal.
## Tareas de desarrollo
- [ ] **T-01 — Detectar compromiso y futuro.** Dificultad: Alto. Regla de dominio/consulta.
- [ ] **T-02 — Implementar edición/eliminación propia.** Dificultad: Alto. API/UI.
- [ ] **T-03 — Probar bloque comprometido.** Dificultad: Alto. Integración y concurrencia aplicable.
## Criterios de aceptación
### CA-01 — Edición futura libre
**Dado** bloque propio futuro sin citas comprometidas, **cuando** se edita con valores válidos, **entonces** agenda se actualiza sin solapes.
### CA-02 — Eliminación futura libre
**Dado** bloque propio futuro libre, **cuando** se elimina, **entonces** deja de ofertarse.
### CA-03 — Protección de reservas
**Dado** bloque con cita/reserva comprometida o bloque pasado, **cuando** se intenta alterar, **entonces** se rechaza.
## Definition of Done
- [ ] CA-01 a CA-03 validados.
- [ ] Ownership, validación temporal e integridad de reserva evidenciados.
- [ ] UI/API y pruebas relevantes registradas.
## Evidencia de validación
| Elemento | Resultado | Evidencia | Observación |
|---|---|---|---|
| CA-01 | Pendiente | — | — |
| CA-02 | Pendiente | — | — |
| CA-03 | Pendiente | — | — |
| DoD | Pendiente | — | — |
## Historial de validación
- 2026-09-17 — Creada en `Borrador`.

