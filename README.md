git-pull-request
================

Git extension to create GitHub Pull Requests

Installation
------------

Just lay `git-pull-request` on your `PATH`.

Usage
-----

You'll need to create a Personal Access Token at https://github.com/settings/applications and put it in the `~/.git-pull-request` file.

```bash
usage: git pull-request -h <branch> -t <title> [options]
   or: git pull-request -h <branch> -i <issue> [options]

Create a Pull Request (PR) in GitHub.

OPTIONS:
   -h <branch>         Branch you want to PR. It has to exist in the remote. Default from "$ git symbolic-ref --short HEAD"
   -r <repo>           Repo where to PR. Default is picked up from "$ git remote -v" origin fetch url.
   -o <owner>          Owner of the repo. Default is picked up from "$ git remote -v" origin fetch url.
   -b <base>           Branch where you want your PR merged into. Default "master".
   -t <title>          Title of the PR.
   -d <description>    Description of the PR.
   -i <issue>          Number of the issue related.
                       WARNING: This will convert the issue into a PR and override <title> and <description>
   -e                  Opens your EDITOR in a temporary file to write the description.
   -c                  Copy the PR URL to the clipboard.
   -f                  Fake run, doesn't make the request but prints the URL and body.

```

The `-c` option requires `xclip` or `pbcopy`.

