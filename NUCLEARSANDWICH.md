# About This Fork #

Hub is pretty sweet, there's no doubt about that. However the standard git and
hub conventions are not to my liking due to both historical reasons and muscle
memory reasons.

- I run my own git/mercurial server in addition to GitHub and as such have kept
  the remote name 'github' for the GitHub project even when it is the canonical
  one.

- I use the remote name 'upstream' for any project on GitHub that is not mine.
  This prevents me from having to know that [rerun][] is an alexch project and
  [renee][] is a renee-project project.

# Differences from upstream/master #

The remote name `github` is used when creating repos, forking a project, or
cloning a project belonging to you. Additionally, the private url is always used
for your own projects.

```
# As nuclearsandwich
$ hub create hyper_home
New repository created nuclearsandwich/hyper_home
git remote add github git@github.com:nuclearsandwich/hyper_home.git

$ hub clone nuclearsandwich/cage
git clone git@github.com:nuclearsandwich/cage.git -ogithub

$ hub fork alexch/rerun
Hardcore forking action...
git remote add github git@github.com:nuclearsandwich/rerun.git
```

The remote name `upstream` is used when cloning another's project on github.

```
# As nuclearsandwich
$ hub clone renee-project/renee
git clone git://github.com/renee-project/renee.git -oupstream
```

# Using This Fork Yourself #

Clone the repo locally and run `rake standalone`. This will build the file `hub`
as a standalone binary in the project root. Then move the binary to wherever you
like. I keep mine in `~/bin/hub`.

[rerun]: https://github.com/alexch/rerun
[renee]: https://github.com/renee-project/renee

