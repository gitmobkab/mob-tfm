## `tfm generate`

Fill a MariaDB/MySQL database table with fake data based on a format string.

Usage:

```
$ tfm generate [OPTIONS] FORMAT
```

Arguments:

- `FORMAT`: A format string that describes the columns and generators to use.

Common options (examples):

- `--seed INTEGER`: Seed for the random generator.
- `--user TEXT`: Database user name.
- `--password TEXT`: Database user password.
- `--database TEXT`: Database name.
- `--table TEXT`: Database table name.
- `--host TEXT`: Database host.
- `--port INTEGER`: Database port (default `3306`).
- `--optimized / --no-optimized`: Use optimized generation methods.
- `--rows INTEGER`: Number of rows to generate.

Behavior:

- The command builds the columns from the format string, generates fake rows and either
	previews them or inserts them into the provided database table.

Example:

```
$ tfm generate "name:firstname() age:int(min=18,max=99)" --rows 50
```

