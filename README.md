# Introduction

This repo aims to give you simple hooks to use for all your git projects.

# What is a git hook ?

A git hook is a script that is activated at a certain time during a git action. For example, during a commit, after a merge, before a push etc.

Hooks are scripts that can be written in different languages, like shell, python or perl.

# Advantages 

This allows, among other things, to force oneself to :
- follow good practices :)
- Automate tasks (lint, formatting, release)
- Warn about possible problems, such as committing secrets
- Synchronize the team on good practices and conventions

# Usage

## Global

1. Create a repo with your hooks.
`mkdir ~/git_hooks`
2. Configure git to recognize your folder
`git config --global core.hooksPath ~/git_hooks`

## Local

In a git repo, the .git/hooks folder contains a set of example hooks. 
Just put your hooks in this folder, respecting the name of the hook type 

## Troubleshoot

- The file must be executable
`chmod +x my_hook`

 
- The file must not have an extension
`mv my_hook.sample my_hook`

- The file must be a hook name recognized by git
`mv commit-message commit-msg`

The list of hook names is available at [git-scm](https://git-scm.com/docs/githooks#_hooks)




