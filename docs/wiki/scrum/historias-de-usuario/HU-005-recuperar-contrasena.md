---
id: HU-005
tipo: historia-de-usuario
titulo: Recuperar contraseña
estado: Borrador
epica: "[[EP-001-identidad-y-perfil]]"
esfuerzo: Alto
sprint_sugerido: "Incremento 1 — Acceso seguro"
dependencias: ["[[HU-002-registrar-usuario]]"]
relacionadas: ["[[HU-004-renovar-y-cerrar-sesion]]"]
---
# HU-005 — Recuperar contraseña
## Historia de usuario
**COMO** usuario registrado  
**QUIERO** solicitar y usar un restablecimiento de contraseña  
**PARA** recuperar el acceso de forma segura.
## Alcance
- Solicitud por email, token temporal de un uso y cambio de password.
## Fuera de alcance
- SMTP obligatorio.
## Reglas de negocio
- Token se consume/invalida al cambiar; en desarrollo puede exponerse solo de forma controlada.
## Dependencias y relaciones
- Épica: [[EP-001-identidad-y-perfil]]; depende de [[HU-002-registrar-usuario]]; relacionada: [[HU-004-renovar-y-cerrar-sesion]].
## Esfuerzo
**Nivel:** Alto. **Justificación:** token de seguridad, expiración y nuevo hash.
## Tareas de desarrollo
- [ ] **T-01 — Modelar token temporal.** Dificultad: Alto. Migración, expiración y un solo uso.
- [ ] **T-02 — Crear solicitud/cambio seguro.** Dificultad: Alto. No revelar existencia de cuenta ni token indebidamente.
- [ ] **T-03 — Construir pantallas y pruebas.** Dificultad: Medio. Solicitud, nueva clave y errores.
## Criterios de aceptación
### CA-01 — Solicitud
**Dado** un email registrado, **cuando** se solicita recuperación, **entonces** se crea un token temporal utilizable por el mecanismo permitido en desarrollo.
### CA-02 — Cambio único
**Dado** token vigente no usado, **cuando** se establece nueva contraseña válida, **entonces** cambia con hash y el token queda consumido.
### CA-03 — Protección
**Dado** token usado, vencido o inválido, **cuando** se intenta cambiar, **entonces** se rechaza sin modificar la contraseña.
## Definition of Done
- [ ] CA-01 a CA-03 validados.
- [ ] Token temporal, expiración, hash y no exposición insegura evidenciados.
- [ ] UI/API y trazabilidad Scrum actualizadas.
## Evidencia de validación
| Elemento | Resultado | Evidencia | Observación |
|---|---|---|---|
| CA-01 | Pendiente | — | — |
| CA-02 | Pendiente | — | — |
| CA-03 | Pendiente | — | — |
| DoD | Pendiente | — | — |
## Historial de validación
- 2026-09-17 — Creada en `Borrador`.

