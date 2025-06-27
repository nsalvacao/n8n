# Architecture Overview

This monorepo contains all packages required to build and run **n8n**.
The most relevant packages are:

- `packages/cli` – command line interface and server entrypoint
- `packages/core` – workflow engine used by the server
- `packages/workflow` – shared workflow interfaces and classes
- `packages/nodes-base` – default nodes shipped with n8n
- `packages/extensions` – mechanism to extend n8n with custom packages
- `packages/frontend` – the editor UI

## Startup process

The script `packages/cli/bin/n8n` loads the configuration, registers nodes and
credentials, sets up the database and then starts the REST API and worker
processes. Running `n8n start` will execute this script.

See the Mermaid diagram [startup.mmd](diagrams/startup.mmd).

## Further reading

- [Execution flow](execution-flow.md)
- [Extensions](extensions.md)
