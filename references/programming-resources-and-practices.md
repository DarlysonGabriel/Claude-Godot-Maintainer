# Programming, debugging, code quality, and Godot references

Use these links as research starting points. Prefer primary documentation, verify versions, and distinguish official documentation from community discussion. Do not imply that every link was consulted for every task.

## General programming documentation

- [MDN Web Docs](https://developer.mozilla.org/) — JavaScript, HTML, CSS, browser APIs, accessibility, and web standards.
- [Microsoft Learn](https://learn.microsoft.com/) — .NET, C#, Windows, Azure, and developer tools.
- [Python Documentation](https://docs.python.org/3/) — Python language and standard library.
- [Java Documentation](https://docs.oracle.com/en/java/) — Java platform and APIs.
- [Rust Documentation](https://doc.rust-lang.org/stable/) — Rust language, standard library, Cargo, and tooling.
- [Go Documentation](https://go.dev/doc/) — Go language and standard library.
- [Kotlin Documentation](https://kotlinlang.org/docs/) — Kotlin language and platform.
- [TypeScript Handbook](https://www.typescriptlang.org/docs/) — TypeScript language and type system.
- [C++ Reference](https://en.cppreference.com/) — C++ language and standard library reference; check the applicable standard version.
- [W3C Standards](https://www.w3.org/standards/) — web standards and accessibility specifications.
- [RFC Editor](https://www.rfc-editor.org/) — Internet protocols and standards.

## Git, collaboration, and project maintenance

- [Pro Git Book](https://git-scm.com/book/en/v2)
- [Git Reference](https://git-scm.com/docs)
- [GitHub Docs](https://docs.github.com/)
- [GitHub Skills](https://skills.github.com/)
- [GitHub Actions](https://docs.github.com/en/actions)
- [GitLab Docs](https://docs.gitlab.com/)
- [Conventional Commits](https://www.conventionalcommits.org/)
- [Keep a Changelog](https://keepachangelog.com/en/1.1.0/)
- [Semantic Versioning](https://semver.org/)

## Code quality, architecture, and security

- [Google Engineering Practices](https://google.github.io/eng-practices/) — code review and engineering practices.
- [Google Documentation Best Practices](https://google.github.io/styleguide/docguide/best_practices.html) — concise, maintained documentation and comments.
- [Google Markdown Style Guide](https://google.github.io/styleguide/docguide/style.html) — consistent Markdown documentation.
- [Martin Fowler](https://martinfowler.com/) — refactoring, architecture, testing, and design.
- [Refactoring.Guru](https://refactoring.guru/) — refactoring techniques and design patterns; use patterns only when they simplify the design.
- [OWASP Developer Guide](https://devguide.owasp.org/) — secure software development guidance.
- [OWASP Cheat Sheet Series](https://cheatsheetseries.owasp.org/) — practical application security guidance.

Practical rules:
- Use clear names and focused functions; make dependencies and side effects visible.
- Prefer the simplest design that meets current requirements; avoid premature abstraction.
- Validate data at trust boundaries and handle errors deliberately.
- Keep secrets out of source code, logs, examples, and commits.
- Preserve public interfaces and serialized formats unless a change is intentional and documented.
- Follow existing formatting and lint conventions; avoid unrelated mass formatting.
- Optimize only after profiling or a reproducible measurement identifies a bottleneck.

## Comments and code documentation

Comments should explain **why**, constraints, invariants, and non-obvious trade-offs—not narrate every line.

- Prefer meaningful names and clear code before adding comments.
- Explain non-obvious decisions, workarounds, algorithmic constraints, and surprising behavior.
- Document public APIs, parameters, return values, side effects, errors, and preconditions where appropriate.
- Keep comments synchronized with code; stale comments are defects.
- Use TODO/FIXME sparingly and include actionable context or an issue reference when possible.
- Do not preserve dead code by commenting it out; remove it through normal review.

Weak comment:
```gdscript
# Increase the score
score += 1
```

Useful comment:
```gdscript
# Keep the multiplier for the entire animation window so input timing
# cannot change the reward midway through the sequence.
combo_score += points * combo_multiplier
```

For GDScript documentation comments and annotations, verify the syntax against the project's Godot version and the official GDScript documentation.

## Debugging methodology

1. Capture the exact error, stack trace, reproduction steps, expected and actual behavior, and environment/version.
2. Reproduce the problem with the smallest reliable example.
3. Locate the failure using breakpoints, call stacks, logs, debugger variables, and targeted instrumentation.
4. Form one hypothesis at a time and identify evidence that would confirm or reject it.
5. Inspect boundaries and state: null/empty values, lifecycle order, async work, resource paths, permissions, and version differences.
6. Change one relevant factor at a time; fix the root cause rather than hiding the symptom.
7. Add a regression test or repeatable validation where practical.
8. Re-run the reproduction and relevant broader checks.
9. Remove temporary logs and instrumentation; report uncertainty honestly.

Never silence an error, disable validation, or weaken security checks merely to hide a symptom.

## Debugging tools

- [GDB Documentation](https://www.gnu.org/software/gdb/documentation/)
- [LLDB](https://lldb.llvm.org/)
- [Chrome DevTools](https://developer.chrome.com/docs/devtools/)
- [Firefox Developer Tools](https://firefox-source-docs.mozilla.org/devtools-user/)
- [Python pdb](https://docs.python.org/3/library/pdb.html)
- [Visual Studio Debugger](https://learn.microsoft.com/en-us/visualstudio/debugger/)
- [Git bisect](https://git-scm.com/docs/git-bisect)
- [Valgrind](https://valgrind.org/docs/)
- [AddressSanitizer](https://clang.llvm.org/docs/AddressSanitizer.html)

## Testing resources

- [Google Testing Blog](https://testing.googleblog.com/)
- [pytest](https://docs.pytest.org/)
- [Python unittest](https://docs.python.org/3/library/unittest.html)
- [Jest](https://jestjs.io/docs/getting-started)
- [Playwright](https://playwright.dev/docs/intro)
- [GUT — Godot Unit Test](https://github.com/bitwes/Gut)
- [GdUnit4](https://github.com/MikeSchulze/gdUnit4)

Choose tests appropriate to the project's architecture. Do not add a test framework without a clear benefit.

## Godot Engine — official resources

- [Godot Documentation, stable](https://docs.godotengine.org/en/stable/)
- [Godot Documentation, Portuguese (Brazil)](https://docs.godotengine.org/pt-br/4.x/)
- [Godot Documentation, latest/development](https://docs.godotengine.org/en/latest/) — may describe unreleased behavior.
- [Godot Class Reference](https://docs.godotengine.org/en/stable/classes/)
- [Step-by-step tutorials](https://docs.godotengine.org/en/stable/getting_started/step_by_step/)
- [Best practices](https://docs.godotengine.org/en/stable/tutorials/best_practices/)
- [GDScript](https://docs.godotengine.org/en/stable/tutorials/scripting/gdscript/)
- [Debugging](https://docs.godotengine.org/en/stable/tutorials/scripting/debug/)
- [Performance](https://docs.godotengine.org/en/stable/tutorials/performance/)
- [2D](https://docs.godotengine.org/en/stable/tutorials/2d/)
- [3D](https://docs.godotengine.org/en/stable/tutorials/3d/)
- [Rendering](https://docs.godotengine.org/en/stable/tutorials/rendering/)
- [Shaders](https://docs.godotengine.org/en/stable/tutorials/shaders/)
- [Physics](https://docs.godotengine.org/en/stable/tutorials/physics/)
- [Navigation](https://docs.godotengine.org/en/stable/tutorials/navigation/)
- [UI](https://docs.godotengine.org/en/stable/tutorials/ui/)
- [Networking](https://docs.godotengine.org/en/stable/tutorials/networking/)
- [Export](https://docs.godotengine.org/en/stable/tutorials/export/)
- [Troubleshooting](https://docs.godotengine.org/en/stable/tutorials/troubleshooting/)
- [Godot Engine source](https://github.com/godotengine/godot)
- [Official demo projects](https://github.com/godotengine/godot-demo-projects)
- [Godot documentation source](https://github.com/godotengine/godot-docs)

## Godot — alternative and community resources

These are community resources, not official Godot documentation. Check maintenance status, engine compatibility, license, dependencies, and renderer support before adopting code or add-ons.

- [Official Godot Forum](https://forum.godotengine.org/)
- [Godot Q&A archive](https://ask.godotengine.org/)
- [Godot Forums (community-run)](https://godotforums.org/)
- [Godot community directory](https://godotengine.org/community/)
- [GDQuest](https://www.gdquest.com/) — tutorials, learning paths, and open-source learning resources.
- [KidsCanCode Godot 4 Recipes](https://kidscancode.org/godot_recipes/4.x/) — practical examples; verify version compatibility.
- [Godot Shaders](https://godotshaders.com/) — community shader examples; inspect licensing, renderer support, and performance.
- [Godot Asset Library](https://godotengine.org/asset-library/) — add-ons, demos, and assets; review permissions and maintenance.
- [GDQuest on GitHub](https://github.com/GDQuest)

## Godot-specific engineering rules

- Detect the exact Godot version and renderer from the project or user input. Do not assume the newest version.
- Match documentation to the project's version. Godot 3 and 4 APIs differ; `latest` may describe unreleased features.
- Verify classes, methods, properties, signals, and annotations in the matching class reference.
- Use the built-in debugger, Output panel, breakpoints, Remote scene tree, profiler, and monitors when relevant.
- Review GDScript typing, inferred types, nullable values, signal lifecycle, node paths, resource loading, and scene ownership.
- Preserve scene/resource UIDs, node paths, ownership, external references, and serialized properties.
- Profile before optimizing; distinguish CPU, GPU, physics, memory, draw-call, and loading costs.
- Check renderer compatibility (Forward+, Mobile, Compatibility), target hardware, import settings, and shader support.
- Validate community snippets and add-ons for compatibility, license, security, maintenance, and performance.
- Do not change visual output, art direction, scene composition, or gameplay feel as an unintended side effect.

## Search patterns

- `site:docs.godotengine.org/en/stable <feature or class>`
- `site:forum.godotengine.org <exact error> <Godot version>`
- `site:github.com/godotengine <API or issue>`
- `site:developer.mozilla.org <web API>`
- `site:stackoverflow.com <exact error> <language/version>`

Link the sources actually consulted and identify relevant versions. Do not imply that every catalog link was consulted for every task.
