## `tfm config`

Create or edit the user configuration used by TFM (stored in the standard OS config directory).

# **Usage**:

```bash
$ tfm config [OPTIONS]
```

# **Options**:

- `--view`, `-v`: Display the current configuration and exit.

# **Behavior**:

- If run without `--view`, the command runs an interactive prompt that lets the user set
	database connection values and defaults for the `generate` and `parse` commands.
- When finished the user can confirm to save the configuration to a JSON file
	
	**Windows: C:\Users\<user>\AppData\Roaming\mob-tfm\config.json**

	**MacOS: ~/Library/Application Support/mob-tfm/config.json**

	**Mac OS X (POSIX): ~/.mob-tfm/config.json**

	**Linux: ~/.config/mob-tfm/config.json**

# **Examples**:

Show current configuration:

```bash
$ tfm config --view
```

Run interactive setup:

```bash
$ tfm config
```

