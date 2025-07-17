
# mcp-server-and-client

This is a Model Context Protocol Server and Client.



## Deployment

Add .vscode folder to it if you are in vscode.

Inside .vscode add file mcp.json.

content inside mcp.json

```bash
    {
  "servers": {
    "test-mcp-video-server": {
      "type": "stdio",
      "command": "node",
      "args": ["build/server.js"],
      "cwd": "${workspaceFolder}",
      "dev": {
        "watch": "build/**/*.js",
        "debug": {
          "type": "node"
        }
      }
    }
  }
}

```

To deploy this project use npm and run

```bash
  "scripts": {
    "server:build": "tsc",
    "server:build:watch": "tsc --watch",
    "server:dev": "tsx src/server.ts",
    "server:inspect": "set DANGEROUSLY_OMIT_AUTH=true && npx @modelcontextprotocol/inspector npm run server:dev",
    "client:dev": "tsx src/client.ts"
  }
```
