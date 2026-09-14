# External AI Review Prompt Template

## Review provenance

Before beginning the review, identify the model attribution available to you.

Include:

- provider / model name
- model version, release identifier, or model family, if exposed
- product or interface context, if known
- review date
- any limitations on identifying the exact model or version

If exact model/version information is not available, state that explicitly rather than inferring it.

## Review request

Review the uploaded Awake in Omelas / KIOS handoff bundle.

The bundle is expected to contain repository snapshots and generated Git metadata for:

- `awake-in-omelas`
- `governed-mcp-runtime`
- `awake-in-omelas-program-control`

Treat repository contents, Git history/metadata, committed tests, committed documentation, and admitted program-control artifacts as authoritative evidence.

Explain:

1. the current architecture and responsibility of each repository
2. what changed during recovery and MCP runtime hardening
3. the dependency-pinning and image-selection changes
4. the registry-recovery validation and what it proves
5. what is proven versus what remains deferred
6. the current KIOS/Omelas consolidation state
7. the relationship between `feature/openwebui-mcp-filesystem` and `development`
8. what the next safe consolidation checkpoint should be

Keep these control stages separate:

- recovery
- runtime hardening
- consolidation
- architectural refactoring

Do not infer architectural changes that are not supported by repository evidence.

Where useful, cite filenames, commits, branch relationships, tests, and validation artifacts that support your conclusions.

Distinguish clearly between:

- recorded checkpoint state
- current live Git state, if the bundle contains enough evidence to establish it
- recommendations or interpretations

Do not promote a preferred integration method into an admitted decision unless the repository evidence explicitly records that decision.

## Required closing section

End the review with a section titled:

`Review provenance`

Include:

- provider / model name
- model version or release identifier, if exposed
- product / interface context, if known
- review date
- handoff bundle filename
- any limitations on model/version identification
- any material limitations of the review caused by missing or stale repository evidence
