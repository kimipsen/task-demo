# Part 06: Grouping Tasks with Namespaces

This demo shows how you can include multiple Taskfiles and group their tasks into namespaces for better organization.

## Files
- `taskfile.dist.yml`: Main Taskfile that includes other Taskfiles with namespaces.
- `infra.dist.yml`: Contains infrastructure-related tasks.
- `app.dist.yml`: Contains application-related tasks.

## How to Use

1. Run `task --list-all` to see all available tasks, grouped by namespace:
   - `infra:setup`, `infra:teardown` (from infra.dist.yml)
   - `app:build`, `app:test` (from app.dist.yml)
   - `greet` (from main Taskfile)

2. Run a namespaced task, e.g.:
   ```
   task infra:setup
   task app:build
   ```

## Notes
- Namespaces help organize tasks from different domains (e.g., infrastructure, application).
- You can add more includes and namespaces as your project grows.
