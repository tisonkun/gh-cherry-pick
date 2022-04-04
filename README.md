# gh-cherry-pick

## Install

```sh
gh extension install tisonkun/gh-cherry-pick
```

## Environment

* (required) `GITHUB_USER`: GH user name, or organization name, if that's where your fork lives.
* (optional) `UPSTREAM_REMOTE` (default: 'upstream')
* (optional) `FORK_REMOTE` (default: 'origin')
* (optional) `GIT_AM_OPTS` (default: '-3'): options when running 'git am'.
* (optional) `SKIP_CONFIRM`: set to 1 to skip all interactive confirmations.
* (optional) `OVERWRITE_PR_TITLE`: set to over the PR title with the given value.
* (optional) `OVERWRITE_PR_BODY`: set to over the PR body with the given value.
* (optional) `EDIT_PR_TITLE`: set to 1 to edit the PR title. 
* (optional) `EDIT_PR_BODY`: set to 1 to edit the PR body.

## Usage

```sh
gh cherry-pick <remote branch> <pr-number>...
```

Cherry pick one or more `<pr>` onto `<remote branch>` and leave instructions for proposing pull request.

Examples:

```sh
gh cherry-pick upstream/release-3.14 12345        # Cherry-picks PR 12345 onto upstream/release-3.14 and proposes that as a PR.
gh cherry-pick upstream/release-3.14 12345 56789  # Cherry-picks PR 12345, then 56789 and proposes the combination as a single PR.
```
