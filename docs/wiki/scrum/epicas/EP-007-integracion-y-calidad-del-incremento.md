---
id: EP-007
tipo: epica
titulo: Integración y calidad del incremento
estado: Borrador
historias: ["[[HU-028-contrato-rest-incremento]]"]
dependencias: ["[[EP-001-identidad-y-perfil]]"]
---
# EP-007 — Integración y calidad del incremento
## Objetivo
Mantener cada incremento aprobado integrable entre frontend y API REST.
## Valor esperado
Contrato verificable sin BFF y evidencia de pruebas aplicables.
## Actores
- USER
- PROFESSIONAL
- ADMIN
## Alcance
- Contrato REST documentado y verificación transversal por incremento.
## Fuera de alcance
- CI/CD obligatorio.
## Reglas de negocio
- API REST JSON directa; CORS explícito; validación de servidor.
## Dependencias
- Todas las HU cross-repo aprobadas.
## Historias de usuario
- [[HU-028-contrato-rest-incremento]]
## Criterio de completitud de la épica
- [ ] Cada funcionalidad cross-repo aprobada tiene contrato y evidencia asociada.
## Riesgos e incógnitas
- Framework frontend pendiente de selección.
