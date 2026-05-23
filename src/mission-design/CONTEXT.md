# Mission Design

Contexto responsable del diseño reusable de las experiencias de juego. Aquí viven las definiciones base que pueden reutilizarse en múltiples sesiones en vivo.

## Language

**Mission**:
Plantilla reusable que define una experiencia de juego. Una **Mission** contiene sus **Mission Stages**, **Hints** y un **Game Type**.
_Avoid_: LiveSession, partida, ejecución

**Mission Stage**:
Paso lineal definido dentro de una **Mission**. Una **Mission Stage** pertenece a una sola **Mission** y expresa el orden base, dificultad y datos de resolución.
_Avoid_: Session Stage, etapa ejecutada

**Hint**:
Pieza de información asociada a una **Mission Stage**. Puede ser visible durante la sesión o revelarse como solución al finalizar.
_Avoid_: Event, evidence, notification

**Game Type**:
Clasificación fija de una **Mission** que determina la estrategia de validación de evidencias. En UMBRAL los valores actuales son Treasure Hunt y Trivia.
_Avoid_: session mode, runtime rule

## Example Dialogue

Dev: "Si una etapa resulta demasiado difícil en una ejecución, ¿edito la Mission?"
Experto de dominio: "No. La Mission conserva el diseño base; el ajuste operativo ocurre en la sesión."

Dev: "Entonces el Game Type pertenece al diseño, no a la operación."
Experto de dominio: "Correcto. La sesión hereda ese tipo desde la Mission."
