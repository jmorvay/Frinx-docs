# Frinx documentation pages

This repository contains three primary resources:

- Our [paths directory](/paths)
- The translations of our popular [Git Cheat Sheets](https://services.github.com/on-demand/downloads/github-git-cheat-sheet.pdf) can be found in the [downloads directory](/downloads). We're always looking for more. 

## heading 2

text:

- We focus on providing clear, step-by-step instructions for completing an activity, giving the learner the opportunity to study the concept in greater detail with the Tell Me Why feature.
- We focus on minimalism.

## Building and Packaging

#### Building and Testing Locally

When you are ready to test your changes, you will want to build the repository locally. This is fully automated through a series of shell scripts based [the scripts to rule them all](https://github.com/github/scripts-to-rule-them-all)!

To perform a build of the materials perform the following:

1. Run `script/setup`
1. Run `script/server`.
    - When successful, the script will initiate a local server at `http://127.0.0.1:4000/on-demand/`.
1. Simply paste that into your favorite web-browser and you will be ready to test.
1. You'll also need to run the following script to compile the SCSS (you can remove the `watch` flag if desired):
```
sass --watch assets/_scss/main.scss:assets/css/main.css
```

> Content based on
> <a href="https://services.github.com/on-demand/">services.github.com/on-demand/</a>
> used under the
> <a href="https://creativecommons.org/licenses/by/4.0/">CC-BY-4.0</a>
> license.</a>

Code used to build and test the site as well as code samples on the site, if any, are licensed under [CC0-1.0](https://creativecommons.org/publicdomain/zero/1.0/legalcode). CC0 waives all copyright restrictions but does not grant you any trademark permissions.

This means you can use the content and code in this repository except for GitHub trademarks in your own projects.

When you contribute to this repository you are doing so under the above licenses.
