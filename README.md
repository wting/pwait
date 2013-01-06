## NAME

pwait - await process completion

## SYNOPSIS

    pwait [pid or process_name...]

## DESCRIPTION

`pwait` waits until all arguments have terminated.

If a number is passed `pwait` assumes it is a pid; otherwise it is
handled as a process name. To wait for a process--not a pid--called "123" use the
`--name` option.

If `pwait` was passed a *process_name* or invoked using the `--name` option,
`pwait` waits until all processes matching *process_name* have terminated,
including new processes spawned after invocation.

Mixing pids and process names is not supported.

The primary difference between `pwait` and `wait` is the latter is limited to
only child processes of the current shell, while `pwait` can be used to monitor
any process.

## OPTIONS

    -i, --interval           set watch interval in seconds (default: 0.1s)

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
