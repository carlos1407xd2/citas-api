---
id: HU-013
tipo: historia-de-usuario
titulo: Crear bloques de disponibilidad
estado: Borrador
epica: "[[EP-003-disponibilidad-profesional]]"
esfuerzo: Alto
sprint_sugerido: "Incremento 3 — Agenda publicable"
dependencias: ["[[HU-010-crear-y-activar-profesionales]]", "[[HU-012-asignar-sedes-profesional]]"]
relacionadas: ["[[HU-014-modificar-bloques-futuros]]", "[[HU-016-consultar-disponibilidad]]"]
---
# HU-013 — Crear bloques de disponibilidad
## Historia de usuario
**COMO** PROFESSIONAL **QUIERO** crear bloques de agenda por día y sede **PARA** publicar horarios reservables.
## Alcance
- Múltiples bloques por día/sede; discretización en slots de 30 min.
## Fuera de alcance
- Bloques pasados, solapados o de sedes no asignadas.
## Reglas de negocio
- RN-06 y RN-07; ejemplo válido 08:00–12:00 y 14:00–17:00.
## Dependencias y relaciones
- Épica: [[EP-003-disponibilidad-profesional]]; depende de [[HU-010-crear-y-activar-profesionales]], [[HU-012-asignar-sedes-profesional]]; relacionadas: [[HU-014-modificar-bloques-futuros]], [[HU-016-consultar-disponibilidad]].
## Esfuerzo
**Nivel:** Alto. **Justificación:** tiempo, solapamiento, sedes, slots y persistencia.
## Tareas de desarrollo
- [ ] **T-01 — Modelar bloque/slots e índices.** Dificultad: Alto. 3FN y consulta de agenda.
- [ ] **T-02 — Aplicar reglas de creación/ownership.** Dificultad: Alto. Dominio, API y UI calendario.
- [ ] **T-03 — Probar pasado, solape y sede.** Dificultad: Alto. Casos de dominio/integración.
## Criterios de aceptación
### CA-01 — Bloque válido
**Dado** PROFESSIONAL activo con sede asignada, **cuando** crea bloque futuro válido, **entonces** queda disponible en slots de 30 minutos.
### CA-02 — Sin solape
**Dado** bloque existente del mismo profesional, **cuando** intenta crear otro que se solapa, **entonces** se rechaza.
### CA-03 — Restricciones
**Dado** fecha pasada o sede no asignada, **cuando** intenta crear bloque, **entonces** se rechaza.
## Definition of Done
- [ ] CA-01 a CA-03 validados.
- [ ] Modelo/migración, índices, ownership y pruebas de reglas evidenciados.
- [ ] Vista y contrato REST actualizados.
## Evidencia de validación
| Elemento | Resultado | Evidencia | Observación |
|---|---|---|---|
| CA-01 | Pendiente | — | — |
| CA-02 | Pendiente | — | — |
| CA-03 | Pendiente | — | — |
| DoD | Pendiente | — | — |
## Historial de validación
- 2026-09-17 — Creada en `Borrador`.

