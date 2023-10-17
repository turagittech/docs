---
title: "pulumi env ls"
aliases:
  - /docs/reference/cli/pulumi_env_ls/
---



List environments.

## Synopsis

List environments

This command lists environments. All environments you have access to will be listed.


```
pulumi env ls [flags]
```

## Options

```
  -h, --help                  help for ls
  -o, --organization string   Filter returned stacks to those in a specific organization
```

## Options inherited from parent commands

```
      --color string                 Colorize output. Choices are: always, never, raw, auto (default "auto")
  -C, --cwd string                   Run pulumi as if it had been started in another directory
      --disable-integrity-checking   Disable integrity checking of checkpoint files
  -e, --emoji                        Enable emojis in the output
      --env string                   The name of the environment to operate on.
      --logflow                      Flow log settings to child processes (like plugins)
      --logtostderr                  Log to stderr instead of to files
      --memprofilerate int           Enable more precise (and expensive) memory allocation profiles by setting runtime.MemProfileRate
      --non-interactive              Disable interactive mode for all commands
      --profiling string             Emit CPU and memory profiles and an execution trace to '[filename].[pid].{cpu,mem,trace}', respectively
      --tracing file:                Emit tracing to the specified endpoint. Use the file: scheme to write tracing data to a local file
  -v, --verbose int                  Enable verbose logging (e.g., v=3); anything >3 is very verbose
```

## SEE ALSO

* [pulumi env](/docs/cli/commands/pulumi_env/)	 - Manage environments

###### Auto generated by spf13/cobra on 17-Oct-2023