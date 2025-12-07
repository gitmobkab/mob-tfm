## `tfm parse`

Load data from a CSV file and insert it into a MariaDB/MySQL database table.

# **Usage**:

```bash
$ tfm parse [OPTIONS] FILE
```

# **Arguments**:

- `FILE`: Path to the CSV file to parse.

# **Options**:

- `-u`, `--user TEXT`: Database user name.
- `-P`, `--password TEXT`: Database user password.
- `-d`, `--database TEXT`: Database name.
- `-t`, `--table TEXT`: Database table name.
- `-h`, `--host TEXT`: Database host. **[default: localhost]**
- `-p`, `--port INTEGER`: Database port. **[default: 3306]**
- `-r`, `--rows INTEGER`: Maximum rows to process, negative value means no limit (only for --no-preview--only) **[default: 20]**.
- `--preview-only / --no-preview-only`: If set, only preview data instead of inserting.

# **Examples**:

```bash
$ tfm parse students.csv --table students --preview-only
```

