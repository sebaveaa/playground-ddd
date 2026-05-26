# Domain Docs

Este repo usa un modelo single-context para consumo de agentes: existe un solo conjunto de documentos de dominio compartidos.

## Leer antes de explorar

- [../product/ers.md](../product/ers.md)
- [../../CONTEXT-MAP.md](../../CONTEXT-MAP.md)
- [../../src/mission-design/CONTEXT.md](../../src/mission-design/CONTEXT.md)
- [../../src/session-operations/CONTEXT.md](../../src/session-operations/CONTEXT.md)
- [../../src/scoring-audit/CONTEXT.md](../../src/scoring-audit/CONTEXT.md)
- [../../src/identity-access/CONTEXT.md](../../src/identity-access/CONTEXT.md)
- `docs/architecture/adr/` cuando exista y sea relevante

## Uso esperado

- El `ERS` define alcance y requerimientos.
- `CONTEXT-MAP.md` define relaciones entre bounded contexts.
- Cada `src/*/CONTEXT.md` define el vocabulario permitido en su contexto.

## Regla principal

Cuando un termino del ERS choque con el lenguaje del contexto, priorizar senalar la discrepancia y no mezclar conceptos.
