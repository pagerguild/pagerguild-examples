# PagerGuild on GitLab CI/CD

# Configuration

- Define database type

  - In the PagerGuild configuration file [`pagerguild.yml`](pagerguild.yml), set the `databaseType` field to the name and version of your production database. See [databases](../../databases/) for additional information.

- Configure access keys

  - OpenAI credentials

    - In your repository CI/CD settings (Project > Settings > CI/CD > Variables), add a `OPENAI_API_KEY` key

  - GitLab credentials

    - In Project > Settings > Access Tokens, create a Project Access Token with configuration:

      - Token name: pagerguild
      - Role: developer
      - Scopes: api

    - In your repository CI/CD settings (Project > Settings > CI/CD > Variables), create a key `GITLAB_TOKEN` with this value, and configuration:

      - Project variable = false
      - Mask variable = true
      - Expand variable = true

# Usage

- PagerGuild will execute on every MR (and MR commit)

- If the MR contains changes to migration or convention files, PagerGuild will run the migration analyzer and post a summary of findings to the MR as a comment
