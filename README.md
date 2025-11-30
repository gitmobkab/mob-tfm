# `tfm`

A set of tools to quick up MySql/MariaDB table prototyping

**Usage**:

```console
$ tfm [OPTIONS] COMMAND [ARGS]...
```

**Options**:

* `--install-completion`: Install completion for the current shell.
* `--show-completion`: Show completion for the current shell, to copy it or customize the installation.
* `--help`: Show this message and exit.

**Commands**:

* `version`: Show the current version of Mob TFM.
* `unspine`: &#x27;Unspine&#x27;/print the doc of a list of tfm...
* `doctor`: Show information about Mob TFM.
* `parse`: fill a mariaDB/MySQL database table with...
* `generate`: fill a mariaDB/MySQL database table with...
* `config`: Create or Edit the configuration for...
* `help`: Open and page the documentation for one or...

## `tfm version`

Show the current version of Mob TFM.

**Usage**:

```console
$ tfm version [OPTIONS]
```

**Options**:

* `--help`: Show this message and exit.

## `tfm unspine`

&#x27;Unspine&#x27;/print the doc of a list of tfm generators inside of a pager (alternative screen)

**Usage**:

```console
$ tfm unspine [OPTIONS] GENERATORS
```

**Arguments**:

* `GENERATORS`: [required]

**Options**:

* `--pretty / --no-pretty`: force activation markdown styling/ may cause issue on old terminals  [default: no-pretty]
* `--help`: Show this message and exit.

## `tfm doctor`

Show information about Mob TFM.
Can be considered as a &#x27;about&#x27; command.

**Usage**:

```console
$ tfm doctor [OPTIONS]
```

**Options**:

* `--help`: Show this message and exit.

## `tfm parse`

fill a mariaDB/MySQL database table with data contained in a csv file.

**Usage**:

```console
$ tfm parse [OPTIONS] FILE
```

**Arguments**:

* `FILE`: [required]

**Options**:

* `-u, --user TEXT`: Database user name  [default: admin]
* `-P, --password TEXT`: Database user password  [default: L2GI2025]
* `-d, --database TEXT`: Database name  [default: tfm_generate]
* `-t, --table TEXT`: The Database Table to target  [default: students]
* `-h, --host TEXT`: The Databse host  [default: localhost]
* `-p, --port INTEGER`: The database port  [default: 3306]
* `-r, --rows INTEGER`: Number of rows to read (can be negative)  [default: 20]
* `--preview-only / --no-preview-only`: If True tfm won&#x27;t try to fill the table, only preview them, default to False  [default: no-preview-only]
* `--help`: Show this message and exit.

## `tfm generate`

fill a mariaDB/MySQL database table with fake data based on a format string.

**Usage**:

```console
$ tfm generate [OPTIONS] FORMAT
```

**Arguments**:

* `FORMAT`: [required]

**Options**:

* `-s, --seed INTEGER`: Seed for the random generator.
* `-u, --user TEXT`: Database user name.  [default: admin]
* `-P, --password TEXT`: Database user password.  [default: L2GI2025]
* `-d, --database TEXT`: Database name.  [default: tfm_generate]
* `-t, --table TEXT`: Database table name.  [default: students]
* `-h, --host TEXT`: Database host.  [default: localhost]
* `-p, --port INTEGER`: Database port.  [default: 3306]
* `--optimized / --no-optimized`: Use optimized generation methods.  [default: no-optimized]
* `-r, --rows INTEGER`: Number of rows to generate.  [default: 20]
* `--help`: Show this message and exit.

## `tfm config`

Create or Edit the configuration for better use of tfm.

**Usage**:

```console
$ tfm config [OPTIONS]
```

**Options**:

* `-v, --view`: View current configuration
* `--help`: Show this message and exit.

## `tfm help`

Open and page the documentation for one or more commands from `docs/commands/README.&lt;command&gt;.md`.

**Usage**:

```console
$ tfm help [OPTIONS] COMMANDS
```

**Arguments**:

* `COMMANDS`: [required]

**Options**:

* `--pretty / --no-pretty`: force activation markdown styling/ may cause issue on old terminals  [default: no-pretty]
* `--help`: Show this message and exit.
