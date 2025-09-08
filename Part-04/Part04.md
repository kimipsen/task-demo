# Demo: Prompts for Environment/Server Actions

This demo shows how to use Taskfile prompts to confirm actions before running commands on specific environments and servers.

## Files
- `taskfile.dist.yml`: Contains tasks that prompt for confirmation before running commands. You select environment/server using variables.

## Instructions
1. Run `task --list-all`
2. Run `task run-command ENV=LX1 SERVER=sup01` to:
   - Specify the environment (LX1, LX2, LX3, LT, ET, FT) and server (ans01, ans02, sup01, sup02, med01, med02, ws01, ws02) as variables.
   - Confirm before running the command.
   - The command will be simulated (echoed).

3. Run `task quick-sup01` for a shortcut to run a command on sup01 in LX1, with a single confirmation prompt.

4. Run `task run-multi ENV=LX3` to run a command on all servers in the specified environment, with a confirmation prompt.
   - The command will be simulated for each server in the list.
5. Run ``task run-multi` to see the difference between passing arguments and falling back to default behavior.

## Notes
- Prompts only support yes/no confirmation, not selection from a list.
- Always pass ENV and SERVER as variables via CLI or environment.
- You can customize the commands and servers as needed for your workflow.
