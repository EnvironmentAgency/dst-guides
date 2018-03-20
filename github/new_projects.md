# New projects

This guide covers how to get a new project on GitHub, and what our standards are for them.

## Get a repo

Contact [Alan Cruikshanks](https://github.com/Cruikshanks) or [David Blackburn](https://github.com/davidblackburn) for a new repo to be created. They'll need

- A name for the project
- A description
- Whether the repo is to be private or public
- Username of who will be its administrator

**Do not create it under your own user account!** Though repo's can be transferred at a later date, it is simpler and clearer if the repo originates within the [Defra](https://github.com/Defra) organisation on GitHub.

## Add a licence and Readme

Before you push your first commit ensure you have added a LICENCE and a README to the project, and that the readme contains our standard sections covering **Contributing to this project** and **About the license**.

The [LICENCE](/LICENSE) and [README](/README.md) files for these guides provide useful examples.

```markdown
## Contributing to this project

Please read the [contribution guidelines](/CONTRIBUTING.md) before submitting a pull request.

## License

THIS INFORMATION IS LICENSED UNDER THE CONDITIONS OF THE OPEN GOVERNMENT LICENCE found at:

<http://www.nationalarchives.gov.uk/doc/open-government-licence/version/3>

The following attribution statement MUST be cited in your products and applications when using this information.

>Contains public sector information licensed under the Open Government license v3

### About the license

The Open Government Licence (OGL) was developed by the Controller of Her Majesty's Stationery Office (HMSO) to enable information providers in the public sector to license the use and re-use of their information under a common open licence.

It is designed to encourage use and re-use of information freely and flexibly, with only a few conditions.
```

## Add a .gitignore

Every project no matter its content should contain a `.gitignore` file. This is to ensure files that are specific to you and the operating system you use are not included as part of the code you are committing to GitHub.

Checkout out <https://github.com/github/gitignore> for a list of useful `.gitignore` templates.

As a minimum always ensure it contains the following

```text
# See https://help.github.com/articles/ignoring-files for more about ignoring files and https://github.com/github/gitignore for some templates
#

# Ignore all logfiles and tempfiles.
/log/*
!/log/.keep
/tmp
*~
.DS_Store
.svn
.*.swp
___*

# Symbol tags (e.g. generated by Atom Editor)
/tags
```

## Protect your branches

Use GitHub's [protected branches](https://help.github.com/articles/about-protected-branches/) feature for `master` (and if you're using Gitflow `develop`).

If you've hooked up the repo to some form of CI that updates the status of commits also use the option [required status checks](https://help.github.com/articles/about-required-status-checks/).