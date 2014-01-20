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

`gitgit repo add <REPO>` introduces `gitgit` to a repository.

`gitgit push` loops through all known repositories and

- for each clean repository, pushes changes upstream; or

- for each dirty repository, displays a message.

`gitgit pull` loops through all known repositories and does the same thing,
but pulls from `origin` instead.

`gitgit repo rm <PATH>` removes a repository from `gitgit`'s configuration.

## configuration

