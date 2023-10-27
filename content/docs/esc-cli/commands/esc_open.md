---
title: "esc open"
---



Open the environment with the given name.

## Synopsis

Open the environment with the given name and return the result

This command opens the environment with the given name. The result is written to
stdout as JSON. If a property path is specified, only retrieves that property.


```
esc open [<org-name>/]<environment-name> [property path] [flags]
```

## Options

```
      --env string          The name of the environment to operate on.
  -f, --format string       the output format to use. May be 'dotenv', 'json', 'detailed', or 'shell' (default "json")
  -h, --help                help for open
  -l, --lifetime duration   the lifetime of the opened environment in the form HhMm (e.g. 2h, 1h30m, 15m) (default 2h0m0s)
```

## SEE ALSO

* [esc](/docs/esc-cli/commands/esc/)	 - Pulumi ESC command line

###### Auto generated by spf13/cobra on 27-Oct-2023