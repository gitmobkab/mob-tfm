## `tfm explain`

Show the detailed documentation for a specific command inside a pager (alternative screen).

# **Usage**:

```bash
$ tfm explain COMMAND [OPTIONS]
```

# **Arguments**:

- `COMMAND`: The command name to view documentation for (for example: `config`, `generate`).

# **Options**:

- `-p`,`--pretty`: Enable extra styling when rendering the markdown (may not work on older terminals).

# **Behavior**:

- Reads the markdown file for the requested command from `docs/commands/README.<command>.md`
	and shows it in a pager for convenient reading.
- If the command is unknown, `tfm explain` will list available commands and exit with an error.

# **Examples**:

```bash
$ tfm explain config
$ tfm explain generate --pretty

# or the very funky but unlikely

$ tfm explain explain -p 
```

