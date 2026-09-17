---
id: HU-004
tipo: historia-de-usuario
titulo: Renovar y cerrar sesión
estado: Borrador
epica: "[[EP-001-identidad-y-perfil]]"
esfuerzo: Alto
sprint_sugerido: "Incremento 1 — Acceso seguro"
dependencias: ["[[HU-003-iniciar-sesion]]"]
relacionadas: ["[[HU-005-recuperar-contrasena]]"]
---
# HU-004 — Renovar y cerrar sesión
## Historia de usuario
**COMO** usuario autenticado  
**QUIERO** renovar mi acceso y cerrar mi sesión  
**PARA** mantener una sesión segura sin reutilizar tokens revocados.
## Alcance
- Refresh con token vigente y logout/revocación.
## Fuera de alcance
- Recuperación de contraseña.
## Reglas de negocio
- Access corto; refresh separado; logout revoca el refresh.
## Dependencias y relaciones
- Épica: [[EP-001-identidad-y-perfil]]; depende de [[HU-003-iniciar-sesion]]; relacionada: [[HU-005-recuperar-contrasena]].
## Esfuerzo
**Nivel:** Alto. **Justificación:** ciclo seguro de tokens entre UI y backend.
## Tareas de desarrollo
- [ ] **T-01 — Persistir/revocar refresh token.** Dificultad: Alto. Modelo normalizado y validación de vigencia.
- [ ] **T-02 — Manejar renovación/cierre en UI.** Dificultad: Medio. Limpieza de sesión y fallo controlado.
- [ ] **T-03 — Probar reutilización y revocación.** Dificultad: Alto. Casos API de token inválido/revocado.
## Criterios de aceptación
### CA-01 — Renovación válida
**Dado** refresh token vigente, **cuando** el access expira y se solicita renovación, **entonces** se entrega un nuevo access según contrato.
### CA-02 — Logout
**Dado** sesión activa, **cuando** el usuario cierra sesión, **entonces** el refresh queda revocado y no permite nueva renovación.
### CA-03 — Token inválido
**Dado** refresh expirado, inválido o revocado, **cuando** se intenta renovar, **entonces** se rechaza y el cliente vuelve a estado no autenticado.
## Definition of Done
- [ ] CA-01 a CA-03 validados.
- [ ] Revocación y expiración verificables sin registrar tokens.
- [ ] Cliente limpia sesión y el contrato queda documentado.
## Evidencia de validación
| Elemento | Resultado | Evidencia | Observación |
|---|---|---|---|
| CA-01 | Pendiente | — | — |
| CA-02 | Pendiente | — | — |
| CA-03 | Pendiente | — | — |
| DoD | Pendiente | — | — |
## Historial de validación
- 2026-09-17 — Creada en `Borrador`.

