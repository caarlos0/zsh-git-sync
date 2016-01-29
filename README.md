# zsh-git-sync [![Build Status](https://travis-ci.org/caarlos0/zsh-git-sync.svg?branch=master)](https://travis-ci.org/caarlos0/zsh-git-sync)

A zsh plugin to sync git repositories and clean them up.

![a gif showing zsh-git-sync in action](https://dl.dropboxusercontent.com/u/247142/projects/git-sync.mov.gif)

## Define `sync`

- prune `origin` or `upstream`;
- merge `upstream` into current branch;
- push merged branch to fork (`origin`);
- remove merged branches.

## Install

### antibody

```console
$ antibody bundle caarlos0/zsh-git-sync
```

### antigen

```console
$ antigen bundle caarlos0/zsh-git-sync
```

## Usage

```console
$ git-sync
```

Or, go ahead and alias it:

```console
$ git config --global alias.sync '!zsh -ic git-sync'
```

Then

```console
$ git sync
```

There is also a public `git-delete-local-merged` function which only deletes
locally merged branches (part of the cleanup thing).

Example:

```console
$ git config --global alias.delete-local-merged '!zsh -ic git-delete-local-merged'
```

Then

```console
$ git delete-local-merged
```

Have fun!
