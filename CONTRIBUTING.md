# Contributing

See [the Shadcn registry docs](https://ui.shadcn.com/docs/registry/getting-started).


## Guidelines

1. Keep changes **source-only** (no builds, no exports)
2. Choose the correct bucket:

   * `ui/` → primitives
   * `components/` → composed UX
   * `lib/` → non-React logic
3. Avoid app- or framework-specific assumptions

All types:

```ts
'registry:base' | 'registry:font' | 'registry:lib' | 'registry:block' | 'registry:component' | 'registry:ui' | 'registry:hook' | 'registry:page' | 'registry:file' | 'registry:theme' | 'registry:style' | 'registry:item' | 'registry:example' | 'registry:internal'
```

## Adding a new item

1. Add files under `ui/`, `components/`, or `lib/`
2. Register the item in `registry.json`
3. Ensure paths are relative and minimal
4. Prefer small, focused items

## Quality bar

1. Deterministic behavior
2. Minimal dependencies
3. Clear naming and foldering

## Updates

* Treat changes as **copy-breaking**
* Assume consumers may have modified the files
* Prefer additive changes over refactors
