# Extensions

n8n can be extended with custom nodes and credentials. The easiest way is to use
`n8n-node-dev` which scaffolds and builds TypeScript nodes.

## Creating a node

1. Run `n8n-node-dev new` to generate a skeleton.
2. Implement the `description` object and the execute method.
3. Build with `n8n-node-dev build` and copy the result to `~/.n8n/custom/` or
   publish as an npm package.

## Publishing an extension package

1. Place your nodes in a package and export them from `index.ts`.
2. Install the package and point `N8N_CUSTOM_EXTENSIONS` to its location or
   install it globally.
3. Restart n8n to load the new nodes.

See [extensions.mmd](diagrams/extensions.mmd) for a simple overview and the
[overview](overview.md) document for repository structure.
