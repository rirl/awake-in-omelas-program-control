# Claude KIOS/Omelas Handoff Review Prompt

Date: 2026-09-13

## Provenance

This file preserves the prompt supplied to Claude for the external review of the Awake in Omelas / KIOS handoff bundle.

Handoff bundle:

```text
awake-in-omelas-handoff-20260913-194033.tar.gz
```

The bundle contained repository snapshots and generated Git metadata for:

- `awake-in-omelas`
- `governed-mcp-runtime`
- `awake-in-omelas-program-control`
- generated Git metadata for each repository
- an `AI-HANDOFF-PROMPT.md`

## Prompt supplied to Claude

Review the uploaded Awake in Omelas / KIOS handoff bundle.

It contains:
- `awake-in-omelas`
- `governed-mcp-runtime`
- `awake-in-omelas-program-control`
- generated Git metadata for each repository
- an `AI-HANDOFF-PROMPT.md`

Treat the repository contents, Git history/metadata, committed tests, and committed documentation as authoritative evidence.

Explain:

1. the current architecture and responsibility of each repository
2. what changed during recovery and MCP runtime hardening
3. the dependency-pinning and image-selection changes
4. the four-phase GHCR registry recovery validation
5. what was proven versus what remains deferred
6. the current KIOS/Omelas consolidation state
7. the relationship between `feature/openwebui-mcp-filesystem` and `development`
8. what the next safe consolidation checkpoint should be

Keep these control steps separate:

- recovery
- runtime hardening
- consolidation
- architectural refactoring

Do not infer architectural changes that are not supported by the repositories.

Where useful, cite filenames and commits that support your conclusions.

## Admission note

This prompt is provenance material for the external Claude review. It does not itself establish authoritative program state, refresh live Git state, or admit an integration decision.
