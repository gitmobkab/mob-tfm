## `tfm config`

Create or edit the user configuration used by TFM (stored in the standard OS config directory).

Usage:

```
$ tfm config [OPTIONS]
```

Options:

- `--view`, `-v`: Display the current configuration and exit.

Behavior:

- If run without `--view`, the command runs an interactive prompt that lets the user set
	database connection values and defaults for the `generate` and `parse` commands.
- When finished the user can confirm to save the configuration to a JSON file
	(typically `~/.config/mob-tfm/config.json`).

Examples:

Show current configuration:

```
$ tfm config --view
```

Run interactive setup:

```
$ tfm config
```

