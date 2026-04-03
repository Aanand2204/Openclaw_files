# 09 Running OpenClaw 24/7 on LocalHost

So, you’ve decided to keep your agent on your local machine—that’s a great choice! It’s free, it’s completely private, and you have 100% control over the hardware. 

But there’s one big challenge: **If your computer sleeps, your agent dies.** In this chapter, we’ll look at the simplest ways to keep OpenClaw running persistently on your laptop or desktop.

---

## ⚡ The "Always Awake" Strategy
To ensure your Cron Jobs (like your morning briefing) actually trigger, your computer needs to be "awake" and connected to the internet at the scheduled time.

### 🪟 For Windows Users
The simplest way to keep your agent alive is to adjust your **Power & Sleep** settings.
1.  Open the **Start Menu** and search for "Power & sleep settings."
2.  Under **Screen and sleep**, change the following:
    *   *On battery power, put my device to sleep after*: **Never** (or a very long time).
    *   *When plugged in, put my device to sleep after*: **Never**.
3.  **Keep it plugged in**: If you're running 24/7 automation, ensure your laptop is connected to a power source.

### 🍎 For Mac Users
macOS is very aggressive about saving power. To prevent it from sleeping:
1.  **The Terminal Trick**: Open your terminal and simply type `caffeinate`. As long as that command is running, your Mac will stay awake.
2.  **Amphetamine (App)**: Download the free "Amphetamine" app from the App Store. It’s a powerful tool that puts a little pill icon in your menu bar—click it to keep your Mac awake indefinitely.

---

## 🏗️ Keeping the Process Alive
OpenClaw runs in your terminal. If you close the terminal window, the "Musketeer" gateway stops.

*   **Dedicated Space**: I recommend keeping a dedicated terminal window open just for OpenClaw. 
*   **Background Run (Mac/Linux)**: If you want to close the window but keep the process, you can use the `nohup` command:
    ```bash
    nohup openclaw start &
    ```

---

## 🔄 Localhost Workflow Visualization
Here is how your local machine handles the agent's constant activity:


``

``

![Diagram](https://mermaid.ink/img/Zmxvd2NoYXJ0IFRECiAgICBVc2VyKFtVc2VyXSkgPC0tPiBMQ1tMb2NhbGhvc3QgQ29udm9dCiAgICBMQyAtLT4gUEMoKFBvd2VyIFNldHRpbmdzKSkKICAgIFBDIC0tPiBPQwogICAgT0NbT3BlbkNsYXcgUnVudGltZV0KICAgIE9DIC0tPiBDUm9uW0Nyb24gSm9icyBBbGl2ZV0=)

---

## ✅ Localhost Success Check
To test if your persistence is working:
1.  Set a Cron Job for 10 minutes from now (e.g., `openclaw cron add "*/10 * * * *" "Ping me to say hello"`).
2.  Wait 10 minutes without touching your computer.
3.  If you get the notification on Telegram, your **Localhost 24/7** setup is perfect!

**Next Lesson:** Now that your "Always On" engine is ready, let’s explore the different ways you can interact with your agent: Web UI, TUI, and Desktop Apps!

