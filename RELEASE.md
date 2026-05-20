# Release Readiness

Agent-Distro owns runnable assembled distributions of AGenNext.

## Boundary

Agent-Distro packages artifacts into runnable distributions. It does not own orchestration, model routing, model execution, or deployment automation internals.

## Release Requirements

- Versioned distro manifests
- Explicit artifact inventory
- Checksums for included artifacts
- Airgap-compatible packaging
- No hidden downloads at runtime
- Reproducible assembly process

## Primitive Rule

A distro is an assembled runnable system made from explicit artifacts.
