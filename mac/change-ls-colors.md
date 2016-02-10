# Change ls colors

`ls -G` on a mac reads from the env var `LSCOLORS`. By default it is set
to `exfxcxdxbxegedabagacad`. Run `man ls` to get a list of different
colors and then export `LSCOLORS` to be something different in your bash
profile.

My current setup:

```bash
export LSCOLORS=ExFxBxDxCxegedabagacad
```
