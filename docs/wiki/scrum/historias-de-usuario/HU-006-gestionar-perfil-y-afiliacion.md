---
id: HU-006
tipo: historia-de-usuario
titulo: Gestionar perfil y afiliación
estado: Borrador
epica: "[[EP-001-identidad-y-perfil]]"
esfuerzo: Alto
sprint_sugerido: "Incremento 1 — Acceso seguro"
dependencias: ["[[HU-001-catalogos-fijos]]", "[[HU-002-registrar-usuario]]"]
relacionadas: ["[[HU-007-gestionar-eps]]", "[[HU-008-gestionar-planes-eps]]"]
---
# HU-006 — Gestionar perfil y afiliación
## Historia de usuario
**COMO** USER autenticado  
**QUIERO** consultar y actualizar mis datos permitidos y afiliación  
**PARA** mantener información necesaria para el agendamiento.
## Alcance
- Perfil permitido y asociación EPS/plan/régimen.
## Fuera de alcance
- Duplicar nombres de catálogos dentro de usuario.
## Reglas de negocio
- Afiliación por relaciones normalizadas; ownership obligatorio.
## Dependencias y relaciones
- Épica: [[EP-001-identidad-y-perfil]]; depende de [[HU-001-catalogos-fijos]], [[HU-002-registrar-usuario]]; relacionadas: [[HU-007-gestionar-eps]], [[HU-008-gestionar-planes-eps]].
## Esfuerzo
**Nivel:** Alto. **Justificación:** perfil protegido y relaciones de afiliación 3FN.
## Tareas de desarrollo
- [ ] **T-01 — Modelar afiliación.** Dificultad: Alto. FKs EPS/plan/régimen, coherencia plan-EPS.
- [ ] **T-02 — Crear consultas/actualización con ownership.** Dificultad: Alto. Validación servidor.
- [ ] **T-03 — Integrar pantalla y pruebas.** Dificultad: Medio. Estados UX y casos inválidos.
## Criterios de aceptación
### CA-01 — Consulta propia
**Dado** USER autenticado, **cuando** consulta perfil, **entonces** ve sus datos permitidos y afiliación sin datos de otros usuarios.
### CA-02 — Actualización válida
**Dado** datos permitidos y referencias activas coherentes, **cuando** actualiza, **entonces** se conservan en su perfil/afiliación.
### CA-03 — Integridad de afiliación
**Dado** un plan que no pertenece a la EPS elegida, **cuando** se intenta asociar, **entonces** se rechaza sin persistir una relación inconsistente.
## Definition of Done
- [ ] CA-01 a CA-03 validados.
- [ ] Migración/FKs 3FN, ownership y pruebas de integridad verificables.
- [ ] Contrato y pantalla documentados.
## Evidencia de validación
| Elemento | Resultado | Evidencia | Observación |
|---|---|---|---|
| CA-01 | Pendiente | — | — |
| CA-02 | Pendiente | — | — |
| CA-03 | Pendiente | — | — |
| DoD | Pendiente | — | — |
## Historial de validación
- 2026-09-17 — Creada en `Borrador`.
