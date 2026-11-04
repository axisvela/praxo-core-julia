# PRAXO-CORE Julia Core

Julia implementation of the PRAXO-CORE contract. This repository is the Julia
package mirror for registration in the General Registry.

- Package: `PraxoCore`
- `SPEC_VERSION`: `0.2.0`
- Core version: `0.2.0`
- Tier: core
- License: MIT
- Dependency: JSON.jl

## Install

After General Registry registration:

```julia
using Pkg
Pkg.add("PraxoCore")
```

Before registration, use this repository directly:

```julia
using Pkg
Pkg.develop(path="path/to/praxo-core-julia")
```

## Scope

`0.2.0` implements all eleven conformance vector groups: tool-call parsing, JSON
Schema, plugin manifests, memory, events, stream kinds, checkpoint envelopes,
path policy, context budgets, middleware, and the agent loop. Provider adapters
remain follow-up work.

## Build and test

```bash
julia --project=. -e 'using Pkg; Pkg.instantiate()'
julia --project=. test/runtests.jl
```

## Layout

- `src/` package source.
- `test/runtests.jl` test suite.
- `Project.toml` package metadata and UUID.

## Release

This mirror uses plain semantic-version tags such as `0.2.0`; the main monorepo
uses `julia/v0.2.0`. Registration is handled by JuliaRegistrator.
