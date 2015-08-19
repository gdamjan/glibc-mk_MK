# glibc mk_MK locale

An extraction of my mk_MK locale from the 
[glibc repository](https://sourceware.org/git/?p=glibc.git;a=history;f=localedata/locales/mk_MK).
This repo is just for my amusement :)

I've contributed this to the glibc project somewhere in 1999/2000.

The extraction is done with a complex `git filter-branch`:
```shell
git clone git://sourceware.org/git/glibc.git
SPELL='git ls-tree -r --name-only --full-tree "$GIT_COMMIT" | grep -v "mk_MK" | tr "\n" "\0" | xargs -0 git rm --cached -r --ignore-unmatch'
git filter-branch --prune-empty --index-filter "$SPELL" -- --all
```
