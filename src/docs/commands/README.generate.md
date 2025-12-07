## `tfm generate`

Fill a MariaDB/MySQL database table with fake data based on a format string.

# **Usage**:

```bash
$ tfm generate [OPTIONS] FORMAT
```

# **Arguments**:

- `FORMAT`: A format string that describes the columns and generators to use.

# **Options (examples)**:

- `-s`, `--seed INTEGER`: Seed for the random generator.
- `-u`, `--user TEXT`: Database user name.
- `-P`, `--password TEXT`: Database user password.
- `-d`, `--database TEXT`: Database name.
- `-t`, `--table TEXT`: Database table name.
- `-h`, `--host TEXT`: Database host. **[default: localhost]**
- `-p`, `--port INTEGER`: Database port **[default `3306`]**.
- `--optimized / --no-optimized`: Use optimized generation methods. (default: --no-optimized)
- `-r`, `--rows INTEGER`: Number of rows to generate. **[default: 20]**

# **Behavior**:

- The command builds the columns from the format string, generates fake rows and either
	previews them or inserts them into the provided database table.

# **Example**:

```bash
$ tfm generate "name:firstname() age:int(min=18,max=99)" --rows 50
```

