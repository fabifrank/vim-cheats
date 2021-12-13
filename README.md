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

## Formatting

### Auto-wrap a long comment line into multiple fixed-width lines

In normal mode, type `gql`. `gq` is the command, while `l` is the motion.
Original:
```
We call this style 'space shuttle style'. Space shuttle style is meant to ensure that every branch and condition is considered and accounted for - the same way code is written at NASA for applications like the space shuttle.
```
Wrapped:
```
We call this style 'space shuttle style'. Space shuttle style is meant to
ensure that every branch and condition is considered and accounted for - the
same way code is written at NASA for applications like the space shuttle.
```
Comment source: [Kubernetes source code](https://github.com/kubernetes/kubernetes/blob/ec2e767e59395376fa191d7c56a74f53936b7653/pkg/controller/volume/persistentvolume/pv_controller.go#L66-L69)\
License: Apache2

## Input/Output

### Save file opened with readonly permission using sudo

See https://stackoverflow.com/questions/2600783/how-does-the-vim-write-with-sudo-trick-work
```
:w !sudo tee %
```

## Windows

`<CTRL-W> W` Switch to next window
