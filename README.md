Design Token System Instructions

Resolution Logic:
1. Always check component tokens first.
2. If value is a reference (e.g. {color.text.default.secondary}),
   resolve it in semantics.json.
3. If semantic maps to another reference, resolve in primitives.json.
4. Continue until a final hex value is reached.
5. Always return final resolved value, not intermediate tokens.

Rules:
- Prefer semantic tokens over primitives.
- Direct primitive usage is allowed only when no semantic mapping exists.

Resolution order:
components → semantics → primitives