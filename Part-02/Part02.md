# Taskfile Priority Rules Example

This directory demonstrates Taskfile priority rules using two Taskfiles:

- `taskfile.dist.yml`: This file is committed to the repository and contains shared tasks.
- `taskfile.yml`: Each user should create this file themselves. It can include user-specific tasks and also import the shared tasks from `taskfile.dist.yml`.

## How to use

1. Before doing anything, run `task --list-all` to see all available tasks. Only 1 should show in the directory, the `hello`-target.

2. Create your own `taskfile.yml` in this directory with the following content:

```yaml
version: '3'
includes:
  base:
    taskfile: ./taskfile.dist.yml
    flatten: true

tasks:
  (insert your own name):
    cmds:
      - echo "This is your personal task!"
    silent: true
```

3. Run `task --list-all` to see all available tasks. You should see both `hello` (from dist) and `mytask` (your own).

4. If you only have `taskfile.dist.yml`, only the shared tasks are available. If you have both, your personal tasks and the shared ones (via include) are available.

## Priority Rules

- If `taskfile.yml` exists, Task will use it and ignore `taskfile.dist.yml` unless you include it.
- If only `taskfile.dist.yml` exists, Task will use it.
- Use the `flatten: true` option to make shared tasks available without a namespace.
