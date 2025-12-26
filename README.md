# Shadcn shared registry

Public source-only registry for sharing **copyable primitives, helpers, and composed components** across repos using `shadcn add`.

See [the Shadcn registry docs](https://ui.shadcn.com/docs/registry).

**What this is**

1. A **shadcn registry**, not a package
2. Files are **copied** into consuming repos
3. Intended for patterns, not runtime libraries

**Structure**

1. `ui/` — design-system primitives (low-level, reusable)
2. `components/` — composed, opinionated components
3. `lib/` — non-React helpers and constants
4. `registry.json` — shadcn registry manifest

**Rules**

1. No app-specific business logic
2. Minimal dependencies
3. Safe to edit after install

**Usage**

In the "framework" folder (eg: `apps/nextjs`) of the client project:

```sh
npx shadcn@latest add \
  https://raw.githubusercontent.com/Labrys-Group/common-registry/main/registry.json\#time
```

See [CONTRIBUTING.md](./CONTRIBUTING.md) on how to contribute.
