# simple-package-manager

For the times when users need to acquire resources for which there is no package management solution,
*simple package manager* facilitates basic package management of a community curated set of packages.


## Installation

1. `git clone git@github.com:DemiCloud/simple-package-manager`
2. `mv simple-package-manager/spkg "${HOME}/.local/bin/spkg"`
3. `chmod 500 "${HOME}/.local/bin/spkg"`


### Updates

`spkg` will be designed to update itself in the future, mitigating the need to re-run the installation process for updates.


### Minimum requirements

- bash 4.4.20 (The version of bash shipped with Ubuntu 18.04 LTS)


## Usage

`spkg` is currently under development, with usable features soon to be delivered.


## Contributions

The team welcomes contributions including but not limited to source-code contributions.
We'd be delighted to hear from you, should you wish to help:

- improve our documentation
- suggest new features
- provide bug-fixes
- test the executable

Please consider adding your suggestion to the project by raising a GitHub issue before submitting
a pull-request.  Pull-requests should reference the issue & vice-versa.


### Minimum quality control

In order to ensure that we always ship a functioning utility which is reliable and maintainable, contributions must be

- tested
- linted with shellcheck
- formatted with shfmt (`shfmt -d -ci -i 2 spkg`)
- adhere to our code-quality standards
(currently, the [Google Bash Style Guide](https://sites.google.com/view/kbocdfydah/google-bash-style-guide))

**Every commit must deliver a functioning executable without exception**.  This does not necessarily
mean a functional change or feature update to `spkg` is included, but the commit must always deliver
a functioning executable so that the repo can be checked-out at any point in it's history with the
expectation of not 'breaking' the utility.  If your single feature is split across multiple commits, 
do they each conform to the parameters set out here, and could they be squashed with `git rebase`?

**A commit should not deliver more than one update** e.g. "Add 2 new commands and overhaul README.md".
Rather, that should be 3 commits, each delivering a "feature".

**Every commit must have an informative commit message** to allow us to understand the purpose at a later date.

**Each commit message should be written as though the changes will take place**, not as though they have
e.g. "Document the behaviour `spkg add`" not "Documented the behaviour `spkg add`".

Frivolous commits for magic internet beans are not welcome.


### Contribution check-list

1. Has the maintenance team accepted your issue and sanctioned a forth-coming pull request?
2. Does your commit add a single feature?
3. Is the commit message descriptive, and helpful?
4. If the contribution is complex, is it well documented for future maintainers?
5. Does the new functionality use the logging system to ensure run-time logging verbosity can be achieved if desired?
6. Do variables names clearly express their purpose?
7. Do the linting and code-quality tools report zero warnings and errors?


### git hooks

The repository has a hooks directory which `git` can be configured to use by executing:

```
git config core.hooksPath hooks
```

A **pre-commit hook** is supplied to:

- analyse project bash files with `shellcheck` and `shfmt`
- analyse README.md using `aspell`

This will assist in preventing malformed files from being committed.  The hook requires a true-colour terminal.
Test your terminal with: `printf 'If the following word is coloured red: \x1b[38;2;255;0;0mcolour!\x1b[0m\n'`


## Contact us

- Join the [Bash Discord Server](https://discord.gg/aD88NDdCrm)
- Send a GitHub Issue

