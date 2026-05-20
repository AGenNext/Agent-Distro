# Agent-Distro

`Agent-Distro` owns runnable AGenNext distributions.

A distro is a curated, assembled, versioned runtime package made from AGenNext artifacts.

It may be small or large. The defining property is not size; the defining property is that it is a runnable assembly.

## What Agent-Distro Produces

Agent-Distro may produce:

- minimal local distro
- single-node distro
- air-gapped distro
- container-image distro
- enterprise install distro

## What A Distro Contains

A distro may contain:

- executables
- container images
- OCI artifacts
- local model artifacts
- skill manifests
- tool manifests
- registry indexes
- startup scripts
- install scripts
- verification scripts
- checksums
- runtime composition manifests

## Core Runtime Shape

```txt
Agent-Kernel
  -> Agent-Runtime
      -> capabilities/tools

Agent-Kernel
  -> model-router
      -> Model-Runner
          -> models
```

## Repo Boundaries

| Repo | Responsibility |
|---|---|
| Agent-Kernel | Orchestration/control loop |
| Agent-Runtime | Capability/tool execution runtime |
| model-router | Model selection and routing |
| Model-Runner | Model execution runtime |
| Agent-Environment | Target host/runtime surface |
| Agent-deploy | Deployment automation |
| Agent-Distro | Runnable assembled distributions |

## Design Rules

A distro must be:

- explicit
- inspectable
- versioned
- reproducible
- runnable
- portable

An air-gapped distro must not require hidden downloads or hosted services at runtime.
