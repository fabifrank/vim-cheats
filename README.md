# vim-cheats

Useful guides for vim: basics, find & replace etc.. 

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

## Input/Output

### Save file opened with readonly permission using sudo

```
# See https://stackoverflow.com/questions/2600783/how-does-the-vim-write-with-sudo-trick-work
:w !sudo tee %
```

## Windows

`<CTRL-W> W` Switch to next window
