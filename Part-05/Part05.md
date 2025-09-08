# Part 05: Dry-Run Mode with Taskfiles

This demo showcases Taskfile's `--dry` argument, which allows you to preview what commands would be executed—without actually running them. This is useful for verifying actions before making changes, especially in scripts that modify files or remote systems.

## How to Use

1. **List available tasks:**
   ```
   task --list-all
   ```

2. **Preview a task without executing:**
   ```
   task --dry <task-name>
   ```
   For example:
   ```
   task --dry deploy
   ```

3. **See the output:**  
   Task will print the commands that would run, but will not execute them.

## Example Tasks
- `deploy`: Deploys the application (simulated)
- `backup`: Backs up the database (simulated)

## Try It Out
- Preview the deploy task:
  ```
  task --dry deploy
  ```
- Preview the backup task:
  ```
  task --dry backup
  ```

- Finish this part by checking the status:
    ```
    task check-tempfile
    ```

This lets you safely check what will happen before running any potentially destructive or important commands.
