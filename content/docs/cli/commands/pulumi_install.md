---
title: "pulumi install"
aliases:
  - /docs/reference/cli/pulumi_install/
---



Install packages and plugins for the current program

## Synopsis

Install packages and plugins for the current program.

This command is used to manually install packages and plugins required by your program.

```
pulumi install [flags]
```

## Options

```
  -h, --help        help for install
      --reinstall   Reinstall a plugin even if it already exists
```

## Options inherited from parent commands

```
      --color string                 Colorize output. Choices are: always, never, raw, auto (default "auto")
  -C, --cwd string                   Run pulumi as if it had been started in another directory
      --disable-integrity-checking   Disable integrity checking of checkpoint files
  -e, --emoji                        Enable emojis in the output
      --logflow                      Flow log settings to child processes (like plugins)
      --logtostderr                  Log to stderr instead of to files
      --memprofilerate int           Enable more precise (and expensive) memory allocation profiles by setting runtime.MemProfileRate
      --non-interactive              Disable interactive mode for all commands
      --profiling string             Emit CPU and memory profiles and an execution trace to '[filename].[pid].{cpu,mem,trace}', respectively
      --tracing file:                Emit tracing to the specified endpoint. Use the file: scheme to write tracing data to a local file
  -v, --verbose int                  Enable verbose logging (e.g., v=3); anything >3 is very verbose
```

## SEE ALSO

* [pulumi](/docs/cli/commands/pulumi/)	 - Pulumi command line

###### Auto generated by spf13/cobra on 26-Oct-2023