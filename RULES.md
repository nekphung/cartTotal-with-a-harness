<!-- A rules file that a stranger could follow —
stack, commands, and at least one "never" —
plus a working gate (npm test and one of
format/lint) and CI running on push. -->
# Project Rules & Development Harness

## Tech Stack
- **Environment:** Node.js (v24)    
- **Language & Module System:** Plain JavaScript (ES Modules, `"type": "module"`)
- **Testing Framework:** Node.js Native Test Runner (`node:test`, `node:assert`)
- **CI:** GitHub Actions

## Verification Commands
- `npm test`: Runs the native test suite locally using `node --test`

## Constraints & Guidelines
- **NEVER** use external third-party dependencies/libraries in `src/cart.js`.
- **NEVER** return prices as formatted strings (e.g., using `.toFixed()`); always return a rounded integer `number`.
- **NEVER** ignore or silence RangeError exceptions for negative prices or non-integer quantities.