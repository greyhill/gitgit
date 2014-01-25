# gitgit

`gitgit` is a utility for `git` to synchronize a ton of repositories.  This
functionality could be implemented in other ways, but whaddyagunnado.

This project is intended to help people who *like* `git` and use it for private
synchronization, but *don't like* manually synchronizing a bunch of
repositories when they switch machines or go home for the day.  `gitgit` tries
to make this task less onerous, so

1. fewer mistakes are made, and

2. programmers resist the temptation to effectively put *all* of `$HOME` under
   a single `git` repository.

## basic usage

By default `gitgit` stores its configuration in `~/.gitgitrc`.  You can change
this for a particular call with the `--config /some/other/rcpath` flag.

### `gitgit repo`

- `gitgit repo add [PATH=.]` introduces `gitgit` to a repository.

- `gitgit repo rm [PATH=.]` removes a repository from `gitgit`'s configuration.

- `gitgit repo list` lists all known repositories.

- `gitgit repo list NEWNAME` changes the nickname for a repository

### `gitgit push`

`gitgit push` loops through all known repositories and

- for each clean repository, pushes changes upstream; or

- for each dirty repository, displays a message.

### `gitgit pull`

`gitgit pull` loops through all known repositories and does the same thing,
but pulls from `origin` instead.


## configuration

