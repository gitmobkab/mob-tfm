## `tfm parse`

Load data from a CSV file and insert it into a MariaDB/MySQL database table.

Usage:

```
$ tfm parse [OPTIONS] FILE
```

Arguments:

- `FILE`: Path to the CSV file to parse.

Common options:

- `--user TEXT`: Database user name.
- `--password TEXT`: Database user password.
- `--database TEXT`: Database name.
- `--table TEXT`: Database table name.
- `--host TEXT`: Database host.
- `--port INTEGER`: Database port.
- `--rows INTEGER`: Maximum rows to process (used for preview/testing).
- `--preview-only / --no-preview-only`: If set, only preview data instead of inserting.

Examples:

```
$ tfm parse students.csv --table students --preview-only
```

