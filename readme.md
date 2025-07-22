This repo holds signatures from the DCO assistent bot for Recheck repos, so the commits don't clutter the main source history.

See `.github/workflows/dco.yml` in those repos for config.

## New repo setup:

1. On the new repo that should require signatures, copy in `.github/workflows/dco.yml` from an existing repo.
   Update `path-to-signatures` and maybe `allowlist`.
2. Create a classic personal access token with the top-level `repo` permission.
   This is overbroad but the bot doesn't (yet?) work with fine-grained tokens.
3. On the new repo, `Settings` -> `Secrets and variables` -> `Actions` -> add a
   new `Repository secret` named `PERSONAL_ACCESS_TOKEN` with the `ghp_....` secret from the previous step.
