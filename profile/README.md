# NuExt

**NuExt** stands for **New Extensions**: pragmatic .NET building blocks for real applications, focused on correctness, predictability, performance, and explicit design.

NuExt provides a lightweight, compile-time-assisted stack for building predictable desktop and hybrid .NET applications without a heavyweight application framework.

## Why NuExt?

- Deterministic synchronous and asynchronous command execution.
- Explicit application, service, view, window, and document lifecycles.
- Compile-time generation of observable properties, commands, validation, and structured localization.
- Practical WPF infrastructure without convention-heavy or reflection-driven runtime machinery.
- Modular packages that can be adopted independently.
- Broad compatibility with modern .NET, .NET Standard, and .NET Framework where applicable.

NuExt favors generated or explicit code over runtime discovery, hidden subscriptions, and convention-based behavior.

## Start here

For WPF and desktop MVVM applications, start with:

- [`NuExt.Minimal.Mvvm`](https://github.com/nu-ext/NuExt.Minimal.Mvvm) for the framework-neutral MVVM core.
- [`NuExt.Minimal.Mvvm.SourceGenerator`](https://github.com/nu-ext/NuExt.Minimal.Mvvm.SourceGenerator) for compile-time properties, commands, validation, and structured localization.
- [`NuExt.Minimal.Mvvm.Wpf`](https://github.com/nu-ext/NuExt.Minimal.Mvvm.Wpf) for WPF application infrastructure.

Additional packages provide reusable WPF behaviors, presentation utilities, MahApps.Metro integration, foundational .NET utilities, and lightweight data-access infrastructure.

## Ecosystem

The graph below shows direct dependencies between NuExt modules:

```text
NuExt.System
└─ NuExt.System.Data
   └─ NuExt.System.Data.SQLite


NuExt.System ─────────────────────┐
NuExt.Minimal.Mvvm ───────────────┤
NuExt.Minimal.Behaviors.Wpf ──────┼─ NuExt.Minimal.Mvvm.Wpf
NuExt.Presentation.Wpf ───────────┘              │
                                                 └─ NuExt.Minimal.Mvvm.MahApps.Metro
```

`NuExt.Minimal.Mvvm.SourceGenerator` is an independent compile-time package with no NuExt package dependencies.

## Projects

### Foundation

- [`NuExt.System`](https://github.com/nu-ext/NuExt.System) — foundational utilities for asynchronous programming, threading, lifetime management, collections, I/O, diagnostics, and BCL compatibility.

### MVVM and desktop applications

- [`NuExt.Minimal.Mvvm`](https://github.com/nu-ext/NuExt.Minimal.Mvvm) — framework-neutral MVVM core with deterministic commands, asynchronous lifecycle management, validation infrastructure, and hierarchical service resolution.
- [`NuExt.Minimal.Mvvm.SourceGenerator`](https://github.com/nu-ext/NuExt.Minimal.Mvvm.SourceGenerator) — compile-time generation of observable properties, commands, validation infrastructure, and structured JSON localization.
- [`NuExt.Minimal.Mvvm.Wpf`](https://github.com/nu-ext/NuExt.Minimal.Mvvm.Wpf) — WPF infrastructure for views, dialogs, documents, windows, dispatchers, application services, and deterministic cleanup.
- [`NuExt.Minimal.Mvvm.MahApps.Metro`](https://github.com/nu-ext/NuExt.Minimal.Mvvm.MahApps.Metro) — MahApps.Metro integration for dialogs and tabbed documents.

### WPF infrastructure

- [`NuExt.Minimal.Behaviors.Wpf`](https://github.com/nu-ext/NuExt.Minimal.Behaviors.Wpf) — reusable WPF behaviors and command interactivity.
- [`NuExt.Presentation.Wpf`](https://github.com/nu-ext/NuExt.Presentation.Wpf) — independent WPF presentation helpers, binding utilities, diagnostics, styles, and control extensions.

### Data access

- [`NuExt.System.Data`](https://github.com/nu-ext/NuExt.System.Data) — lightweight data-access utilities and abstractions.
- [`NuExt.System.Data.SQLite`](https://github.com/nu-ext/NuExt.System.Data.SQLite) — SQLite integration and database context infrastructure.

## Design principles

NuExt follows several consistent principles across its packages:

1. **Correctness before convenience**  
   APIs define explicit lifecycle, ownership, synchronization, and error-handling behavior.

2. **Predictable runtime behavior**  
   Commands, services, validation, view resolution, and cleanup avoid hidden control flow.

3. **Compile-time assistance**  
   Source generation removes boilerplate without shifting behavior into reflection-heavy runtime machinery.

4. **Performance by design**  
   Hot paths avoid unnecessary allocations, repeated reflection, and mutable shared state.

5. **Modular adoption**  
   Packages remain focused and can be used independently without adopting the entire ecosystem.

## Packages

NuExt packages are available from the [NuExt profile on NuGet](https://www.nuget.org/profiles/NuExt).

Each repository contains package-specific documentation, supported target frameworks, usage examples, and release information.