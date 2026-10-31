# Repository maintenance workflows


## Debugging workflow

- [ ] Capture the exact error, stack trace, reproduction steps, expected/actual behavior, and environment.
- [ ] Reproduce with the smallest reliable example.
- [ ] Use breakpoints, call stacks, debugger state, and targeted logs rather than guessing.
- [ ] Test one hypothesis at a time and fix the root cause.
- [ ] Add regression coverage where practical and rerun relevant checks.
- [ ] Remove temporary instrumentation and report remaining uncertainty.

## Code quality and review workflow

- [ ] Review correctness and observable behavior first.
- [ ] Check naming, function responsibilities, cohesion, coupling, duplication, and side effects.
- [ ] Review error handling, validation, security boundaries, and resource cleanup.
- [ ] Prefer simple local improvements over speculative abstractions.
- [ ] Avoid unrelated formatting or broad rewrites.
- [ ] Report actionable findings with file/line references and concrete failure scenarios.

## Comments and documentation workflow

- [ ] Prefer clear names and code over comments that narrate obvious operations.
- [ ] Explain rationale, invariants, constraints, workarounds, and non-obvious decisions.
- [ ] Document public APIs, parameters, return values, side effects, and errors where appropriate.
- [ ] Keep comments accurate; remove stale comments and commented-out dead code.
- [ ] Keep TODO/FIXME notes actionable and contextualized.

## Godot debugging and profiling workflow

- [ ] Confirm engine version, renderer, OS, and target hardware where relevant.
- [ ] Inspect the script, scene, resource, signal, and node path involved.
- [ ] Use Godot debugger, Output, breakpoints, Remote scene tree, and profiler.
- [ ] Check lifecycle order, resource loading, signal connections, and scene ownership.
- [ ] Profile before optimizing and identify CPU, GPU, physics, memory, or loading bottlenecks.
- [ ] Verify in the target engine version and renderer while preserving visuals and gameplay.
