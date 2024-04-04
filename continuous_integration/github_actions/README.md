# PagerGuild on Github Actions

# Configuration

- Define database type

  - In the PagerGuild configuration file [`pagerguild.yml`](pagerguild.yml), set the `databaseType` field to the name and version of your production database. See [databases](../../databases/) for additional information.

- Configure access keys

  - Can be configured at the repository level (recommended) or the organization level

  - Define the following secrets in "Settings > Security > Secrets and variables > Actions":

    - `OPENAI_API_KEY`

# Usage

- PagerGuild will execute on every PR (and PR commit)

- If the PR contains changes to migration or convention files, PagerGuild will run the migration analyzer and post a summary of findings to the PR as a comment
