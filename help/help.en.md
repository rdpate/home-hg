Home Hg
====

Manage ~/.hg symlink to .home-hg while running the given Mercurial command.

Quick Setup
----

    # from scratch
    hg init
    mv .hg .home-hg

    # ignore untracked files
    printf %s\\n 'syntax: glob' '*' >>~/.hgignore
    hhg add .hgignore

Example
----

    $ hg root
    abort: no repository found in '/home/roger' (.hg not found)!
    $ hhg root
    /home/roger

Manual Management
----

The two commands "hhg-activate" and "hhg-release" are what handle the symlink; "hhg" is a wrapper around them and Mercurial.  "hhg-activate" and "hhg-release" can be executed manually or as an hhg subcommand, eg. "hhg hhg-activate".
