# 09 Web UI, TUI & Desktop: Choosing Your Command Center

One of the coolest parts of OpenClaw is that it isn’t just a background process—it’s a living tool you can control in multiple ways. Whether you want a high-end dashboard, a retro terminal interface, or a distraction-free desktop app, OpenClaw has you covered!

---

## 🌐 The Web UI (Dashboard)
The Web UI is where most people start. It’s built on **React and Vite** and gives you a beautiful, visual control panel.

### How to access it:
1.  Run the following command in your terminal:
    ```bash
    openclaw web
    ```
2.  **The Token Security**: When the terminal opens, it will give you a link that looks like this: 
    `http://localhost:3000/?token=abc123xyz...`
3.  **Don't just copy the URL**—copy the **entire link with the token**. If you don't use the token, the dashboard will say "Unauthorized."

### Features:
*   **Real-time Chat**: Test your agent in the browser before deploying to Telegram.
*   **Dark Mode/Light Mode**: Full customization for your workspace.
*   **Zen Mode**: Remove all distractions and just talk to your assistant.

---

## ⌨️ The TUI (Terminal User Interface)
For the hardcore developers and terminal lovers, there is the **TUI**. 

### How to access it:
```bash
openclaw tui
```

### Why use the TUI?
The TUI is **much deeper** than the Web UI. It offers **46+ commands** hidden behind the `/` (slash) key.
*   **Slash Commands**: Press `/` to see a massive list of options: `/help`, `/status`, `/models`, `/agents`, etc.
*   **Advanced Control**: You can manually switch "brains" (models), reset sessions, and view detailed logs much faster than clicking through a browser.

---

## 🖥️ The Desktop App
Finally, there is the standalone **Desktop App**. This is perfect if you want your assistant separate from your browser tabs. It supports a **Zen Mode** that mimics the minimal design of premium AI tools.

---

## 🔄 Interaction Diagram
Here’s a look at how these different frontends connect to the same OpenClaw backend:

<details>
<summary>View Mermaid Source</summary>

```mermaid
graph LR
    OC((OpenClaw Backend)) -- API/WebSocket --> Web[Web UI (React)]
    OC -- RPC --> Desktop[Desktop App]
    OC -- CLI --> TUI[Terminal UI]
```

![Diagram](https://mermaid.ink/img/Z3JhcGggTFIKICAgIE9DKChPcGVuQ2xhdyBCYWNrZW5kKSkgLS0gQVBJL1dlYlNvY2tldCAtLT4gV2ViW1dlYiBVSSAoUmVhY3QpXQogICAgT0MgLS0gUlBDIC0tPiBEZXNrdG9wW0Rlc2t0b3AgQXBwXQogICAgT0MgLS0gQ0xJIC0tPiBUVUlbVGVybWluYWwgVUld)
</details>

---

## ✅ Interface Success Check
The best way to learn is to **try each one**. Launch the Web UI first, then try the TUI. See which one feels more natural for your workflow. 

**Next Lesson:** Let's look at the secret sauce behind your agent—the "Identity," "Soul," and "Memory" files!
