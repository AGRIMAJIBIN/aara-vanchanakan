# Aara Vanchanakan — ആരാ വഞ്ചകൻ?

An original browser-based 3D Kerala village social deduction game for 4–10 players.

The complete game source is included in `game-source.tar.gz`. Extract it to inspect or develop the game:

```sh
tar -xzf game-source.tar.gz
npm install
npm start
```

Open http://localhost:3000. Solo exploration is also available from the menu.

## Render deployment

- Service type: Web Service
- Runtime: Node
- Build command: `tar -xzf game-source.tar.gz && npm install --omit=dev`
- Start command: `node server.js`
- Health check: `/health`
- Instances: 1
- Environment: `NODE_ENV=production`, `NODE_VERSION=22`

The server uses the host-provided PORT, serves both the frontend and Socket.IO, and keeps active rooms in memory. Restarts end active games.

Original procedural 3D assets and synthesized audio are included in the source. Frontend: Three.js. Backend: Node.js, Express, Socket.IO.
