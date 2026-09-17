---
id: HU-016
tipo: historia-de-usuario
titulo: Consultar disponibilidad
estado: Borrador
epica: "[[EP-004-reserva-y-ciclo-de-cita]]"
esfuerzo: Alto
sprint_sugerido: "Incremento 4 — Cita general"
dependencias: ["[[HU-009-gestionar-especialidades]]", "[[HU-011-asignar-especialidades-profesional]]", "[[HU-012-asignar-sedes-profesional]]", "[[HU-013-crear-bloques-disponibilidad]]"]
relacionadas: ["[[HU-017-reservar-cita-general]]", "[[HU-018-solicitar-cita-especializada]]"]
---
# HU-016 — Consultar disponibilidad
## Historia de usuario
**COMO** USER **QUIERO** filtrar horarios disponibles por sede, tipo, especialidad, profesional y fecha **PARA** elegir una franja realmente reservable.
## Alcance
- Filtros del RF-10 y solo slots que completan duración requerida.
## Fuera de alcance
- Confirmar la reserva.
## Reglas de negocio
- Especialidad activa/asignada; 60 min exige dos slots consecutivos libres; no mostrar pasado.
## Dependencias y relaciones
- Épica: [[EP-004-reserva-y-ciclo-de-cita]]; depende de [[HU-009-gestionar-especialidades]], [[HU-011-asignar-especialidades-profesional]], [[HU-012-asignar-sedes-profesional]], [[HU-013-crear-bloques-disponibilidad]]; relacionadas: [[HU-017-reservar-cita-general]], [[HU-018-solicitar-cita-especializada]].
## Esfuerzo
**Nivel:** Alto. **Justificación:** filtros, reglas de elegibilidad y slots consecutivos.
## Tareas de desarrollo
- [ ] **T-01 — Definir consulta de disponibilidad eficiente.** Dificultad: Alto. Índices, filtros y datos 3FN.
- [ ] **T-02 — Aplicar duración/elegibilidad.** Dificultad: Alto. Dominio/API.
- [ ] **T-03 — Implementar buscador UI.** Dificultad: Medio. Estados vacío/error y filtros.
- [ ] **T-04 — Probar 30/60 y reservas.** Dificultad: Alto. Casos consecutivos/no disponibles.
## Criterios de aceptación
### CA-01 — Filtros
**Dado** oferta publicada, **cuando** USER filtra por cualquiera de los criterios RF-10, **entonces** recibe solo horarios que coinciden.
### CA-02 — Duración completa
**Dado** especialidad de 60 minutos, **cuando** consulta disponibilidad, **entonces** solo se muestran inicios con dos slots consecutivos libres.
### CA-03 — Elegibilidad
**Dado** profesional/especialidad inactivo o no asociado, **cuando** se consulta, **entonces** no se ofrece ese horario.
## Definition of Done
- [ ] CA-01 a CA-03 validados.
- [ ] Consulta/indexación, reglas 30/60 y pruebas de integridad de slots evidenciadas.
- [ ] Buscador y contrato REST documentados.
## Evidencia de validación
| Elemento | Resultado | Evidencia | Observación |
|---|---|---|---|
| CA-01 | Pendiente | — | — |
| CA-02 | Pendiente | — | — |
| CA-03 | Pendiente | — | — |
| DoD | Pendiente | — | — |
## Historial de validación
- 2026-09-17 — Creada en `Borrador`.

