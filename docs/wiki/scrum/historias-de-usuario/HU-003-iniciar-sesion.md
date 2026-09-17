---
id: HU-003
tipo: historia-de-usuario
titulo: Iniciar sesión
estado: Borrador
epica: "[[EP-001-identidad-y-perfil]]"
esfuerzo: Alto
sprint_sugerido: "Incremento 1 — Acceso seguro"
dependencias: ["[[HU-002-registrar-usuario]]"]
relacionadas: ["[[HU-004-renovar-y-cerrar-sesion]]"]
---
# HU-003 — Iniciar sesión
## Historia de usuario
**COMO** usuario registrado  
**QUIERO** iniciar sesión con email y contraseña  
**PARA** acceder solo a las capacidades de mi rol.
## Alcance
- Autenticación y emisión separada de access/refresh JWT.
## Fuera de alcance
- Renovación y revocación, tratadas en [[HU-004-renovar-y-cerrar-sesion]].
## Reglas de negocio
- Roles hacen parte del contexto de autorización; no loguear tokens/passwords.
## Dependencias y relaciones
- Épica: [[EP-001-identidad-y-perfil]]; depende de [[HU-002-registrar-usuario]]; relacionada: [[HU-004-renovar-y-cerrar-sesion]].
## Esfuerzo
**Nivel:** Alto. **Justificación:** Spring Security/JWT, roles y manejo de sesión UI.
## Tareas de desarrollo
- [ ] **T-01 — Definir autenticación y autorización.** Dificultad: Alto. Access/refresh separados y secretos por environment.
- [ ] **T-02 — Integrar pantalla de login.** Dificultad: Medio. Estados loading/error y protección de ruta según contrato.
- [ ] **T-03 — Probar credenciales y roles.** Dificultad: Alto. Rechazos y contexto autorizado.
## Criterios de aceptación
### CA-01 — Credenciales correctas
**Dado** un usuario activo con contraseña válida, **cuando** inicia sesión, **entonces** recibe sesión con access y refresh diferenciados y su rol.
### CA-02 — Credenciales inválidas
**Dado** email inexistente o contraseña incorrecta, **cuando** inicia sesión, **entonces** se rechaza sin revelar secretos ni crear sesión.
### CA-03 — Autorización
**Dado** una sesión válida, **cuando** accede a una capacidad protegida, **entonces** se aplica el rol correspondiente.
## Definition of Done
- [ ] CA-01 a CA-03 con evidencia de pruebas de autenticación/autorización.
- [ ] Secrets configurables, sin logs de credenciales/tokens, y CORS explícito verificables.
- [ ] Flujo UI/API y contrato REST trazados.
## Evidencia de validación
| Elemento | Resultado | Evidencia | Observación |
|---|---|---|---|
| CA-01 | Pendiente | — | — |
| CA-02 | Pendiente | — | — |
| CA-03 | Pendiente | — | — |
| DoD | Pendiente | — | — |
## Historial de validación
- 2026-09-17 — Creada en `Borrador`.

