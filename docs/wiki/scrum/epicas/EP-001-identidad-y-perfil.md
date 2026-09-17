---
id: EP-001
tipo: epica
titulo: Identidad y perfil
estado: Borrador
historias: ["[[HU-001-catalogos-fijos]]", "[[HU-002-registrar-usuario]]", "[[HU-003-iniciar-sesion]]", "[[HU-004-renovar-y-cerrar-sesion]]", "[[HU-005-recuperar-contrasena]]", "[[HU-006-gestionar-perfil-y-afiliacion]]"]
dependencias: []
---
# EP-001 — Identidad y perfil
## Objetivo
Permitir acceso seguro y la administración de los datos permitidos del USER.
## Valor esperado
Base de identidad y autorización para capacidades posteriores.
## Actores
- USER
## Alcance
- Registro, JWT access/refresh, recuperación, perfil y afiliación.
## Fuera de alcance
- Datos clínicos y correo SMTP obligatorio.
## Reglas de negocio
- Email y documento únicos; password con hash adaptativo; secrets fuera del código.
## Dependencias
- Ninguna externa al alcance; usa [[HU-001-catalogos-fijos]].
## Historias de usuario
- [[HU-001-catalogos-fijos]]
- [[HU-002-registrar-usuario]]
- [[HU-003-iniciar-sesion]]
- [[HU-004-renovar-y-cerrar-sesion]]
- [[HU-005-recuperar-contrasena]]
- [[HU-006-gestionar-perfil-y-afiliacion]]
## Criterio de completitud de la épica
- [ ] Todas sus HU obligatorias están `Completada` con evidencia.
- [ ] Autorización por rol y ownership verificables.
## Riesgos e incógnitas
- Definir contrato seguro de exposición controlada del token de recuperación en desarrollo.
