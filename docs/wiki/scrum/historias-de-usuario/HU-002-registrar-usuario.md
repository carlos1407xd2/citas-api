---
id: HU-002
tipo: historia-de-usuario
titulo: Registrar usuario
estado: Borrador
epica: "[[EP-001-identidad-y-perfil]]"
esfuerzo: Alto
sprint_sugerido: "Incremento 1 — Acceso seguro"
dependencias: ["[[HU-001-catalogos-fijos]]"]
relacionadas: ["[[HU-003-iniciar-sesion]]"]
---
# HU-002 — Registrar usuario
## Historia de usuario
**COMO** visitante  
**QUIERO** crear una cuenta USER  
**PARA** acceder al agendamiento con mi identidad ficticia.
## Alcance
- Nombres, apellidos, tipo/número documento, email, teléfono y contraseña.
## Fuera de alcance
- Creación autónoma de ADMIN o PROFESSIONAL.
## Reglas de negocio
- Email y documento únicos; password jamás texto plano; datos sintéticos.
## Dependencias y relaciones
- Épica: [[EP-001-identidad-y-perfil]]; depende de [[HU-001-catalogos-fijos]]; relacionada: [[HU-003-iniciar-sesion]].
## Esfuerzo
**Nivel:** Alto. **Justificación:** identidad, validaciones, persistencia, seguridad y UI/API.
## Tareas de desarrollo
- [ ] **T-01 — Modelar usuario y constraints.** Dificultad: Alto. Migración Flyway 3FN, únicos de email/documento.
- [ ] **T-02 — Implementar caso de uso seguro.** Dificultad: Alto. Validación servidor, hash adaptativo y autorización de rol.
- [ ] **T-03 — Construir formulario del frontend elegido.** Dificultad: Medio. Estados de validación, error y éxito.
- [ ] **T-04 — Probar duplicados y secreto.** Dificultad: Medio. Dominio/API sin exponer password.
## Criterios de aceptación
### CA-01 — Registro válido
**Dado** datos mínimos válidos y únicos, **cuando** el visitante confirma registro, **entonces** se crea una cuenta con rol USER.
### CA-02 — Unicidad
**Dado** email o documento ya registrados, **cuando** se intenta registrar, **entonces** se rechaza claramente sin crear duplicado.
### CA-03 — Protección de contraseña
**Dado** un registro exitoso, **cuando** se revisa la persistencia y respuesta, **entonces** la contraseña no está en texto plano ni se devuelve.
## Definition of Done
- [ ] CA-01 a CA-03 validados con pruebas relevantes.
- [ ] Migración Flyway, constraints únicos y hash adaptativo verificables.
- [ ] Formulario y contrato REST documentados; no hay secretos/PII reales.
## Evidencia de validación
| Elemento | Resultado | Evidencia | Observación |
|---|---|---|---|
| CA-01 | Pendiente | — | — |
| CA-02 | Pendiente | — | — |
| CA-03 | Pendiente | — | — |
| DoD | Pendiente | — | — |
## Historial de validación
- 2026-09-17 — Creada en `Borrador`.

