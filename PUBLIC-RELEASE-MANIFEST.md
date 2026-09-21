# Public Release Manifest

This file defines the intended public boundary for the Fourth Man repository. It is a release-control document, not a record of private pilot execution.

## Allowed public files

The first public release may contain only these files:

- `.gitignore`
- `LICENSE`
- `README.md`
- `SKILL.md`
- `LIMITATIONS.md`
- `PUBLIC-RELEASE-MANIFEST.md`

Any additional file requires an explicit review before it is added to a release.

## Always exclude

Do not copy or publish:

- evaluator keys, answer keys, scoring rubrics, or held-out expected findings;
- private pilot cases, source packets, source ledgers, manifests, prompts, assignments, or run outputs;
- private journals, gate records, reviews, change-control records, or workspace status files;
- credentials, tokens, private keys, personal data, patient information, confidential material, or local configuration;
- provider authentication, internal client, retry, logging, diagnostic, or profile implementation details;
- absolute local filesystem paths or unrelated workspace documents;
- generated logs, reports, archives, caches, editor state, and temporary files.

## Release review

Run these checks from the repository root before a release commit:

```bash
git status --short --branch --untracked-files=all
git ls-files
git diff --check
git log --all --name-only --format=
git fsck --full --no-reflogs
git tag --list
```

Review the complete working tree and reachable history for credentials, private paths, personal data, evaluator material, pilot references, provider internals, and unsupported medical claims. Record only pass/fail and remediation categories; do not commit raw scan output.

Verify the release from a clean checkout or archive. A successful local commit is not a publication. Push or change repository visibility only after explicit human authorization, then verify the remote commit, tag, rendered documentation, and file list from a fresh clone.
