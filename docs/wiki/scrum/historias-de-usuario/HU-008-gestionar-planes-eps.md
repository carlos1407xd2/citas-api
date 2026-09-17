---
id: HU-008
tipo: historia-de-usuario
titulo: Gestionar planes de EPS
estado: Borrador
epica: "[[EP-002-catalogos-y-profesionales]]"
esfuerzo: Medio
sprint_sugerido: "Incremento 2 — Oferta configurable"
dependencias: ["[[HU-007-gestionar-eps]]"]
relacionadas: ["[[HU-006-gestionar-perfil-y-afiliacion]]"]
---
# HU-008 — Gestionar planes de EPS
## Historia de usuario
**COMO** ADMIN **QUIERO** gestionar planes asociados a una EPS **PARA** ofrecer afiliaciones consistentes.
## Alcance
- Crear, consultar, actualizar y desactivar plan por EPS.
## Fuera de alcance
- Plan sin EPS válida.
## Reglas de negocio
- Un plan mantiene FK a EPS; no se borra físicamente si está referenciado.
## Dependencias y relaciones
- Épica: [[EP-002-catalogos-y-profesionales]]; depende de [[HU-007-gestionar-eps]]; relacionada: [[HU-006-gestionar-perfil-y-afiliacion]].
## Esfuerzo
**Nivel:** Medio. **Justificación:** relación padre-hijo, estado lógico y UI/API protegida.
## Tareas de desarrollo
- [ ] **T-01 — Modelar plan dependiente de EPS.** Dificultad: Medio. FK y únicos pertinentes.
- [ ] **T-02 — Gestionar y filtrar por EPS.** Dificultad: Medio. API/UI ADMIN.
- [ ] **T-03 — Probar integridad y desactivación.** Dificultad: Medio. Casos referenciados.
## Criterios de aceptación
### CA-01 — Asociación obligatoria
**Dado** ADMIN y EPS activa, **cuando** crea un plan válido, **entonces** el plan queda asociado a esa EPS.
### CA-02 — Coherencia de consulta
**Dado** planes configurados, **cuando** se consulta una EPS, **entonces** solo se listan sus planes aplicables según contrato.
### CA-03 — Conservación
**Dado** plan usado en afiliación, **cuando** ADMIN lo desactiva, **entonces** no se elimina su referencia histórica.
## Definition of Done
- [ ] CA-01 a CA-03 validados.
- [ ] Relación 3FN/FK, autorización y pruebas verificables.
- [ ] Contrato y trazabilidad actualizados.
## Evidencia de validación
| Elemento | Resultado | Evidencia | Observación |
|---|---|---|---|
| CA-01 | Pendiente | — | — |
| CA-02 | Pendiente | — | — |
| CA-03 | Pendiente | — | — |
| DoD | Pendiente | — | — |
## Historial de validación
- 2026-09-17 — Creada en `Borrador`.

