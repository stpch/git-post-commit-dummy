# git-post-commit-dummy

A Git `post-commit` hook that keeps your GitHub commit graph intact. 

Saves all commits to non-owned repositories to your own repository as dummy commit (message only), so you don't lose the commits when you're removed from the project or organization.

## Installation

1. Create a new repository (e.g. `git-history`) in your GitHub account that will be used as dummy commit target
2. Clone the repository to your local machine and note its path
3. Download [post-commit](post-commit) and set `GITHUB_ACCOUNT_URL` and `DUMMY_COMMIT_REPOSITORY`
4. Make `post-commit` executable by running `chmod +x post-commit`
5. Copy `post-commit` to a project's `.git/hooks` directory to have it save dummy commits
