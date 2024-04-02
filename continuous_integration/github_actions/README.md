# PagerGuild on Github Actions

# Installation

- Install the PagerGuild Github Action

  - Copy-paste the [pagerguild_review.yml](pagerguild_review.yml) workflow file into your repository's `.github/workflows/` folder

- Configure access keys

  - Can be configured at the repository level (recommended) or the organization level

  - Define the following secrets in "Settings > Security > Secrets and variables > Actions":

    - `OPENAI_API_KEY`

# Usage

- PagerGuild will execute on every PR (and PR commit)

- If the PR contains changes to migration or convention files, PagerGuild will run the migration analyzer and post a summary of findings to the PR as a comment
