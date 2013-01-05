## NAME

pwait - await process completion

## SYNOPSIS

    pwait [pid...]

    pwait -n [process_name...]

## DESCRIPTION

`pwait` waits until all *pid* arguments have terminated.

If `pwait` was invoked using the `--name` option, `pwait` waits until all
processes matching *process_name* have terminated, including new processes
spawned after invocation.

The primary difference between `pwait` and `wait` is the latter is limited to
only child processes of the current shell, while `pwait` can be used to monitor
any process.

## OPTIONS

    -i, --interval           set watch interval in seconds (default: 0.1)

    -n, --name               watch process based on exact name rather than pid

    -v, --verbose            increase verbosity

    -vv                      increase verbosity more

    --version                show version number and exit

## INSTALLATION

- download [pwait](https://github.com/wting/pwait/raw/master/pwait)

        $ wget https://github.com/wting/pwait/raw/master/pwait

- make it executable

        $ chmod +x ./pwait

- move it to a folder in `$PATH`

        $ mv ./pwait ~/bin/

## RELATED

proctools, wait

## LICENSE

Copyright (c) 2013, William Ting. Licensed under BSD 2-clause:
<http://opensource.org/licenses/BSD-2-Clause>.
