# pkg-changesets
Package creation using changesets to manage the releases

## How to work with this way of creating packages

1. Create a branch
2. Make changes
3. Commit changes and push the branch
4. Once all changes are done, run `pnpm changeset` to create a changeset specifying the changes you made *
4. Create a PR
5. Merge the PR

Do the previous steps for each change you want in the next release.

* You also can commit to the main branch if it's not protected, but you will have to create a PR with all the changesets, running the command `pnpm changeset` for each change you have made.

## How to create a release

1. Each time you have executed the `pnpm changeset` command, you generate a new file in the `.changeset` folder. This file contains the changes you made and the version you want to release. You can edit this file to change the version you want to release.

2. When some files inside the `.changeset` folder are detected in the main branch, a new Pull Request is created, where the changes are summarized in the CHANGELOG.md and the version is updated. This PR is created by the `changeset-bot` user.

3. Once the PR is merged, the changes are published to npm and the release is created in GitHub.




