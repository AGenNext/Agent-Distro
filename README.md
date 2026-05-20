# Agent-Kit

`Agent-Kit` owns portable AGenNext runtime kits.

A kit is a packaged set of components, manifests, scripts, and artifacts that can run AGenNext in a specific environment.

## Purpose

`Agent-Kit` is the middle layer between source code and runtime environment.

```txt
source repos
  -> Agent-Kit
  -> target environment
```

## Responsibilities

`Agent-Kit` owns:

- air-gapped bundles
- local development kits
- single-node install kits
- enterprise install packages
- portable manifests
- offline verification scripts
- runtime composition scripts
- model/skill/tool packaging references

## Not Responsibilities

`Agent-Kit` does not own:

- capability orchestration
- model routing
- model execution
- tool implementation
- environment provisioning
- deployment automation internals

## Core Component Flow

```txt
Agent-Kernel
  -> model-router
  -> Model-Runner
  -> local model artifacts
```

## Repo Boundaries

| Repo | Responsibility |
|---|---|
| Agent-Kernel | Capability orchestration |
| model-router | Model selection and routing |
| Model-Runner | Model execution/runtime |
| Agent-deploy | Deployment automation |
| Agent-Environment | Target runtime surface |
| Agent-Kit | Portable runtime kits |

## Design Rule

A kit must be explicit, portable, inspectable, and runnable without hidden cloud dependencies.
