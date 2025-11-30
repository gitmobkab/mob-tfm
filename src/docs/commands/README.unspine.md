## `tfm unspine`

Open and page the documentation for one or more generator files located in `docs/generators/`.

Usage:

```
$ tfm unspine GENERATORS [OPTIONS]
```

Arguments:

- `GENERATORS`: One or more generator names separated by spaces (e.g. `name firstname`).

Options:

- `--pretty`: Enable extra styling when rendering the markdown.

Behavior:

- For each generator name provided the command reads `docs/generators/README.<generator>.md`
	and opens it in a pager.
- If an unknown generator is requested the command prints an error and lists available generators.

Example:

```
$ tfm unspine name firstname
```

