# Context Map

## Contexts

- [Mission Design](./src/mission-design/CONTEXT.md) - define el diseño reusable de misiones, etapas y pistas.
- [Session Operations](./src/session-operations/CONTEXT.md) - opera sesiones en vivo, equipos, estado y flujo efectivo de etapas.
- [Scoring and Audit](./src/scoring-audit/CONTEXT.md) - calcula puntajes, registra penalizaciones, mantiene ranking e historial auditable.
- [Identity and Access](./src/identity-access/CONTEXT.md) - contexto de soporte para autenticación, autorización y administración de usuarios operativos.

## Relationships

- **Mission Design -> Session Operations**: Session Operations usa una Mission activa como plantilla para crear una LiveSession y derivar su Session Stage Flow.
- **Session Operations -> Scoring and Audit**: Session Operations entrega evidencias validadas y penalizaciones para cálculo sincrónico de puntaje, y además emite hechos relevantes para trazabilidad.
- **Scoring and Audit -> Session Operations**: Scoring and Audit devuelve resultados de puntaje para el flujo observable de la sesión y mantiene el historial auditable como preocupación separada.
- **Identity and Access -> Mission Design**: Identity and Access provee identidades y roles para autorizar acciones administrativas sobre misiones.
- **Identity and Access -> Session Operations**: Identity and Access provee identidades y roles para autorizar acciones operativas y acceso participante.
