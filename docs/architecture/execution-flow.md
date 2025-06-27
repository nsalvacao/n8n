# Execution Flow

This document explains how a workflow runs inside n8n.

1. A workflow is triggered by an API call, schedule or event.
2. The workflow definition is loaded from the database.
3. The execution is queued and picked up by the workflow runner.
4. Nodes and credentials used in the workflow are resolved.
5. Each node executes following the connections defined in the workflow.
6. Items are passed from node to node until the end is reached.
7. Execution data and logs are persisted, and hooks emit events.

Refer to the sequence diagram [execution-flow.mmd](diagrams/execution-flow.mmd).

See the [overview](overview.md) for general information about the repository.
