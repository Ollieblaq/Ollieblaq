# Profile token setup (to do later)

The 3D contribution city is rebuilt daily by `.github/workflows/profile-3d.yml`.
It uses the `PROFILE_TOKEN` secret if it exists, and falls back to the default
`GITHUB_TOKEN` (which only sees public activity).

To count private contributions too:

1. GitHub > Settings > Developer settings > Personal access tokens > Tokens (classic).
2. Create a token with `read:user` scope (add `repo` to include private repo activity).
3. In this repo: Settings > Secrets and variables > Actions > New repository secret.
4. Name it `PROFILE_TOKEN` and paste the token.
5. Actions tab > "profile-3d" workflow > Run workflow.
