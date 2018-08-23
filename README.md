# git-post-commit-dummy

A Git `post-commit` hook that keeps your GitHub (or other) commit graph intact. 

Saves all commits to non-owned repositories to your own repository as dummy
commit (commit without changes), so you don't lose the commits when removed from
the project or organization.

Dummy commit messages have the following format:

```
Original commit subject

https://url-to-non-owned-repository
```

## Installation

1. Create a new remote repository (e.g. `git-history`) that will be used as dummy commit target
2. Clone the repository to your local machine and note its path
3. Download [post-commit](post-commit) and set `OWNED_REMOTE_URL_PREFIX` and
`DUMMY_COMMIT_REPOSITORY_PATH`
4. Make `post-commit` executable by running `chmod +x post-commit`
5. Copy `post-commit` to a project's `.git/hooks` directory to have it save
dummy commits

## Check that it works

1. Create a local commit for a project with `post-commit` installed
2. Check that your dummy commit repository (e.g. `git-history`) received the
dummy commit
