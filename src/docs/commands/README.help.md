## `tfm help`

Show the detailed documentation for a specific command inside a pager (alternative screen).

Usage:

```
$ tfm help COMMAND [OPTIONS]
```

Arguments:

- `COMMAND`: The command name to view documentation for (for example: `config`, `generate`).

Options:

- `--pretty`: Enable extra styling when rendering the markdown (may not work on older terminals).

Behavior:

- Reads the markdown file for the requested command from `docs/commands/README.<command>.md`
	and shows it in a pager for convenient reading.
- If the command is unknown, `tfm help` will list available commands and exit with an error.

Examples:

```
$ tfm help config
$ tfm help generate --pretty
```

