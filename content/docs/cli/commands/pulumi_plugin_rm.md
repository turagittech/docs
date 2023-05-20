---
title: "pulumi plugin rm"
aliases:
  - /docs/reference/cli/pulumi_plugin_rm/
---



Remove one or more plugins from the download cache

### Synopsis

Remove one or more plugins from the download cache.

Specify KIND, NAME, and/or VERSION to narrow down what will be removed.
If none are specified, the entire cache will be cleared.  If only KIND and
NAME are specified, but not VERSION, all versions of the plugin with the
given KIND and NAME will be removed.  VERSION may be a range.

This removal cannot be undone.  If a deleted plugin is subsequently required
in order to execute a Pulumi program, it must be re-downloaded and installed
using the plugin install command.

```
pulumi plugin rm [KIND [NAME [VERSION]]] [flags]
```

### Options

```
  -a, --all    Remove all plugins
  -h, --help   help for rm
  -y, --yes    Skip confirmation prompts, and proceed with removal anyway
```

### Options inherited from parent commands

```
      --color string                 Colorize output. Choices are: always, never, raw, auto (default "auto")
  -C, --cwd string                   Run pulumi as if it had been started in another directory
      --disable-integrity-checking   Disable integrity checking of checkpoint files
  -e, --emoji                        Enable emojis in the output
      --logflow                      Flow log settings to child processes (like plugins)
      --logtostderr                  Log to stderr instead of to files
      --non-interactive              Disable interactive mode for all commands
      --profiling string             Emit CPU and memory profiles and an execution trace to '[filename].[pid].{cpu,mem,trace}', respectively
      --tracing file:                Emit tracing to the specified endpoint. Use the file: scheme to write tracing data to a local file
  -v, --verbose int                  Enable verbose logging (e.g., v=3); anything >3 is very verbose
```

### SEE ALSO

* [pulumi plugin](/docs/cli/commands/pulumi_plugin/)	 - Manage language and resource provider plugins

###### Auto generated by spf13/cobra on 19-May-2023