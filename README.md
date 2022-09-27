# Testing Release Please

## Conventional commit messages used as a standard for generating the change log.
https://www.conventionalcommits.org/en/v1.0.0/

## Run via GitHub Actions
1. Action can be triggered via any action event e.g. in the case of this repo, it triggers off a merge to the main branch.
2. Creates a new PR to the main branch (pretty sure this can be triggered via) - this PR is created when it spots "releasable units" in the commit history being merged. 
A releasable unit is a commit to the branch with one of the following prefixes: "feat", "fix", and "deps"
This PR contains a generated changelog, including increments to major, minor and patch numbering.
3. Version number can be updated via an empty commit with the appropriate body (i.e. `git commit --allow-empty -m "chore: release 2.0.0" -m "Release-As: 2.0.0"`)
4. Commit messages for the changelog can also be fixed via: 

## Next: Java - what does it do currently to snapshot versions