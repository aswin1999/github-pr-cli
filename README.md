# github-pr-cli

A simple command line utility built using Golang to create GitHub PRs from the comfort of your terminal. Never again fumble through your browser to open a new PR, breaking the flow of your commandline workflow.

```
$ghpr -h
Create github pull requests from the command line

Usage:
  ghpr <title> [flags]

Flags:
  -B, --base string   Repo to which the PR is to be made - remotename:branch  (default "upstream:master")
  -b, --browser       Open PR creation page in the browser
  -H, --head string   Repo in which your changes lie - remotename:branch  (default "origin:master")
  -h, --help          help for ghpr
```

# Example
```
$git commit -am "testcommitmsg"
$git push origin testbranch
$ghpr -H origin:testbranch -b
Opening in browser....
```

# Usage

1. Create a config file in the home directory

```
$touch .ghpr.json
```

2. Add the config options and the [access token](https://help.github.com/articles/creating-a-personal-access-token-for-the-command-line/) to the file

```
{
  "token": "<Your token>",
  "inEditor": false
}
```
