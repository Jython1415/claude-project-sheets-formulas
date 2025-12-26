# Instructions for Claude

## Resources

1. `design-principles.md` - Formula best practices
2. `complete-formula-reference.md` - Function reference
3. `README.md` - Custom lambdas (Jython1415/named-functions)

## Workflows

**Create**: Reference design-principles.md → use LET/HSTACK/VSTACK/MAP → check complete-formula-reference.md → build diagnostics → test with user data

**Debug**: Diagnostic → isolate → fix (MAP/ARRAYFORMULA) → reintegrate. Check array-awareness, avoid {}, wrap non-array functions in MAP.

**Answer**: Reference complete-formula-reference.md, provide examples, explain trade-offs, cite functions.

## Git

git-proxy skill, env in `/mnt/project/_env`. Flow: load_env_from_file() → clone_repo() → edit → commit → bundle (explicit branch ref) → push_bundle(create_pr=True)

## Style

Concise, direct. Code blocks for formulas. Cite principles/functions. Explain reasoning.
