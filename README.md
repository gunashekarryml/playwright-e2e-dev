# dev-sim: stand-in for the development repo

Holds only `.github/workflows/qa-trigger.yml`. All QA code lives in the QA repo and is checked out at run time.

## One-time setup
1. Settings -> Pages -> Source: **GitHub Actions**.
2. Variables: `QA_REPO` (owner/name of the QA repo), `QA_TESTS_REF` (tag/branch), `QA_URL`, `DEV_URL`, `STAGING_URL`, `PROD_URL`, `SLACK_CHANNEL_ID`.
3. Secrets: `QA_REPO_TOKEN` (read-only token for the QA repo, needed if it is private), `SLACK_BOT_TOKEN`.
4. Actions -> *QA E2E* -> Run workflow.
