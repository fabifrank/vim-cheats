# vim-cheats

## Working Directory

`:pwd` show current working directory
`:cd <PATH>` change current working directory

## Find & Replace

### Replace `foo` with `bar` in multiple files in folder

```sh
# set the folder to look up
:cd <FOLDER>
# find files ending in .yml
:vimgrep /foo/g **/*.yml
# show matching files
:copen
# replace foo with bar (the "c" will let you confirm each match)
:cfdo %s/foo/bar/gc | update
```

## Windows

`<CTRL-W> W` Switch to next window
