# Fork maintenance

This fork (`ababber/atlas-lean`) tracks upstream `facebookresearch/atlas-lean`.

## Sync from upstream

```bash
git fetch upstream --prune
git merge upstream/main
git push origin main
```

## Pre-commit guard

This fork has a pre-commit hook (`.githooks/pre-commit`) that blocks internal vocabulary from being committed. The guard prevents accidental exposure of shadow-architecture patterns.

**Blocked content:**
- Internal kit files (`.cursorrules`, `.toolrules`, etc.)
- Shadow-architecture patterns and vocabulary
- References to private shadow repos

**Override (emergency only):**
```bash
SKIPPUBLISHABLEGUARD=1 git commit ...
```

## Related

- **Private lane:** `ababber/shadow-atlas-lean` — for experiments and notes
- **Upstream:** `facebookresearch/atlas-lean`
- **AutoformBot:** `facebookresearch/autoform-bot` — the pipeline that generated ATLAS
