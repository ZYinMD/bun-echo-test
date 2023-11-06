This is the demo repo to reproduce the bun issue https://github.com/oven-sh/bun/issues/6929

To reproduce:

1. Have docker engine running
1. In VSCode, install the "Dev Containers" extension published by Microsoft.
1. Command palette `Dev Containers: Clone Repository in Container Volume`, paste in the url of this repo `https://github.com/ZYinMD/bun-echo-test`
1. Wait till container spins up.
1. Open vscode integrated terminal, now you're inside the container.
1. `bun install && bun dev` to start the vite dev server.
1. Press `q` or `ctrl-c` to stop vite.
1. The bug should now have reproduced - can no longer see what you type.
1. blindly type `reset` or `stty echo` to recover

You could also test locally, just clone the repo and skip to step 6, but it may not reproduce.
