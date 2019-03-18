# Git Release Log

This command line utility is great for generating a list of PRs from GitHub with a given repository and label the PR is tagged with.

## Installation

```bash
gem install graphql-client
git clone git@github.com:king601/git-release-log.git
cd git-release-log && cp git-release-log /usr/local/bin/
```

You'll need to setup a GitHub Personal Access Token in your gitconfig:

**Note: Ensure your access token has full repo access!**

```bash
git config --global integrate.github-token <insert token here>
```

## Usage

```bash
git release-log -r owner/repo
```

Example output:
```
===============
repo has 1 Total PRs with the Label 'release'
===============
[ATHENS-001] Testing improvements to Application
```

You can specify a different label with the `--label` or `-l` flag.

```bash
git release-log -r ProctorU/cloud-functions -l 'Deployed: Staging'`
```

Example output:
```
===============
cloud-functions has 1 Total PRs with the Label 'Deployed: Staging'
===============
[CF-001] Add handleMorningAssignments function
```

## Need Help?

You can view the commands built in help with the following command:

```bash
git release-log -h
```
