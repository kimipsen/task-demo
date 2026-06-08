# Readme

This repository exists to showcase some powerful features in Taskfiles; how it can be helpful to share commands and how to hide long, difficult commands behind short aliases.

## Demos

The following demos are available:

* [Part 01](Part-01/Part01.md): Shows how preconditions work and how a single well-placed taskfile can work in several directories.
* [Part 02](Part-02/Part02.md): Shows how priority rules picks which taskfile to load and how users can create custom targets while including repository-specific targets also.
* [Part 03](Part-03/Part03.md): Shows how commands may be OS-specific
* [Part 04](Part-04/Part04.md): Shows how commands can be passed arguments, can trigger prompts to ensure you really do want to execute commands and how arguments may be configured with multiple values. It also shows how targets can have descriptions, which show can listing all commands.
* [Part 05](Part-05/Part05.md): Shows how it is possible to run targets with the `--dry` argument to see what happens, without executing the actual commands.
* [Part 06](Part-06/Part06.md): Shows how multiple taskfiles can be included into a single list and targets stored in namespaces, to show what they relate to.
* [Part 07](Part-07/Part07.md): Shows how to specify enums and how the interactive terminal helps/handles arguments.