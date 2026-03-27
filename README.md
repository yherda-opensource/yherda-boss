# Yherda Boss Vault

Local belief system design environment — Yherda stand-in until the platform is live.

## Structure

- `belief-systems/` — compressed belief system artifacts; each file is a canonical belief system
- `workspaces/` — decompressed working files; iterative design space before compression
- `bootstrap-prompts/` — final bootstrap prompts derived from belief systems; what users receive

## The Pattern

1. Decompress ideas into `workspaces/`
2. Compress into a belief system in `belief-systems/`
3. Derive bootstrap prompt in `bootstrap-prompts/`
4. User pastes prompt → Claude reads it → context is set

## Migration

When Yherda is ready, belief system files migrate there. Bootstrap prompts update to point at Yherda. User experience is continuous.
