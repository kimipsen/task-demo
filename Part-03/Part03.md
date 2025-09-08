# OS-Specific Tasks Demo

This demo shows how Taskfile can run different tasks depending on the operating system.

## Files
- `taskfile.dist.yml`: Contains tasks restricted to Linux, macOS, or Windows using the `platforms:` key.

## Instructions
1. Run `task --list-all` to see all available tasks.
2. Run `task os-info`, `task os-info-mac`, or `task os-info-win` in this directory.
   - Only the task matching your OS will run; others will be skipped.


## Notes
- The `platforms:` key restricts tasks to specific operating systems.
- The `.dist.` moniker allows you to keep shared tasks in version control.
