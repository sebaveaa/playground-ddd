# Operating Model

Modelo operativo común para agentes que trabajen en este repo.

## Fuentes de verdad

Leer en este orden:

1. [../product/ers.md](../product/ers.md)
2. [../../CONTEXT-MAP.md](../../CONTEXT-MAP.md)
3. [../architecture/repo-structure.md](../architecture/repo-structure.md)
4. `src/*/CONTEXT.md` según el bounded context afectado
5. `docs/architecture/adr/` cuando exista una decisión relevante

## Reglas

- Usar el vocabulario exacto de los `CONTEXT.md`.
- Si el ERS contradice un `CONTEXT.md`, reportar la contradicción antes de proponer código.
- No asumir carpetas de implementación que no existan todavía.
- Diferenciar documentación de dominio, documentación operativa y skills.
- Si falta una decisión de arquitectura difícil de revertir, proponer un ADR.

## Estado actual del repo

- `src/` contiene el mapa de contextos del proyecto y su lenguaje.
- `.agents/` contiene skills y utilidades del runtime.
- `docs/agents/` contiene agentes esperados para la construcción del proyecto.
- El repo todavía no define la estructura final de implementación del monorepo.
