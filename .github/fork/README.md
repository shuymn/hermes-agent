# Fork sync

This standalone repository uses `main` as a generated distribution branch:

1. Start from the latest `v*` tag in `NousResearch/hermes-agent`.
2. Apply every patch in `.github/fork/patches/` with `git am`.
3. Restore `.github/fork/` and `.github/workflows/` from the fork checkout.
4. Run the targeted update tests.
5. Push the generated tree to `main`.

Runtime clones should use this repository as `origin` and should not keep an
`upstream` remote. Official upstream access is isolated to the sync workflow.
