# git-test-project-fixture (IT1.16 test fixture — GitHub boundary)

Per PS-97 v1.1 §1.1.5 (closed-loop boundary-fixture pattern).

This repository is an operational artefact. It exists solely as a stable real-remote target for
`git-mcp-server` integration tests (IT1.9, IT1.10, IT1.14, IT1.16) running against the GitHub
boundary (`github.com`). The repository on the Gitea boundary mirror
(`gitea.cloud-dog.net/test-fixtures/git-test-project`) carries the equivalent minimal shape so
the same test suite can exercise either boundary without code changes.

## Shape (do not remove without coordinating with IT1.* test maintainers)

- `main` branch: README.md, .gitattributes, file1.txt, file2.txt, file3.txt (3 commits on top of
  the GitHub auto-init initial commit).
- `develop` branch: adds `docs/note.md` on top of main (1 extra commit).
- Tag `v0.0.1` on the "seed" commit.

No secrets, no LFS, no submodules.
