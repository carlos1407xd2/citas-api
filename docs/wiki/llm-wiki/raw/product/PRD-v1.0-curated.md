# Fuente RAW: PRD v1.0 (curada)

- Origen: `/PRD.md`
- Versión declarada: 1.0
- Tipo: especificación de producto

## Claims preservados

- Sistema académico ficticio de agendamiento; no usa datos privados reales de FCV.
- Actores: USER, PROFESSIONAL y ADMIN.
- Incluye registro, JWT access/refresh, recuperación, perfiles/afiliación, catálogos, profesionales, disponibilidad, citas generales y especializadas, cancelación, reprogramación, auditoría y agendas por rol.
- Citas generales se aprueban automáticamente; especializadas requieren aprobación administrativa.
- Los slots son de 30 minutos; una especialidad puede requerir 30 o 60 minutos.
- El frontend consume REST directamente desde Spring Boot; no existe BFF.

Este snapshot es una referencia curada; el texto completo permanece en la fuente original.
