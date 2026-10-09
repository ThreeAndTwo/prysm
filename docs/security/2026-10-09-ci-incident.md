# CI incident containment — 2026-10-09

Repository: `ThreeAndTwo/prysm`
Branch: `develop`
Inspected head: `0ec2cf67c5d4011b665652b12a7ce5de23b23639`

Actions were disabled before this cleanup. Keep them disabled until the repository owner explicitly approves restoration.

The owner confirmed that this personal repository must not contain GitHub Actions workflows. This change removes every file under `.github/workflows` on this branch, regardless of its name.

Files removed in this change:

- `.github/workflows/go.yml` — original Git object `5f179de5c95699b14e62a3ae089cc6df2a6a3b88`.
- `.github/workflows/horusec.yaml` — original Git object `b5bf9831b8a911bc9be526250fb115f1c23b8161`.
- `.github/workflows/security-audit.yml` — original Git object `a5a0cbcf7f5aa30b5ac499d441e7ecc089fd1ea5`.

Evidence and limits

- Unauthorized workflows were observed attempting credential or repository-history disclosure. A successful workflow run alone does not prove data receipt or credential validity.
- Existing Git history is retained as evidence. No release, tag, force push, or history rewrite is part of this cleanup.
- Revoking a GitHub token does not rotate credentials issued by other services.
- The initial credential compromise and the authentication method used for the mass write remain under investigation.
- This record supersedes any earlier note suggesting that personal-repository workflows should be retained.
