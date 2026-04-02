# 15 Cron Jobs vs Heartbeats: Automation Logic

Most AI chatbots are **reactive**—they sit there and wait for you to speak. But what if your assistant could start a conversation with *you*? That is the power of **Cron Jobs** and **Heartbeats**.

In this chapter, we’re going to give your agent a "sense of time."

---

## ⏰ Cron Jobs: The "Alarm Clock" Logic
A **Cron Job** tells your agent to do something at a specific, fixed time every day, week, or month.

*   **Example**: Every morning at 9:00 AM, send me a Telegram message with my to-do list.
*   **Transcript Logic**: During the crash course, we asked the agent: *"Can you remind me every morning at 9:00 AM to start my day with a to-do list?"*
*   **Behind the Scenes**: OpenClaw created a Cron Job file that triggers the agent automatically at that exact timestamp.

### ⌨️ CLI Command Example:
```bash
# Add a daily reminder at 9:00 AM
openclaw cron add "0 9 * * *" "Summarize the top tech news from Tavily and send it to me over Telegram."
```

---

## 💓 Heartbeats: The "Pulse" Logic
A **Heartbeat** is slightly different. Instead of a fixed time, it’s a repeating interval.

*   **Example**: Every 30 minutes, check my Gmail for urgent emails.
*   **Why use it?**: This is perfect for monitoring systems where you don't care *when* it happens, just that it happens *often*.

---

## 🔄 Proactive Mechanism Diagram
Here is how your agent manages these automated triggers:


``

``

![Diagram](https://mermaid.ink/img/Z3JhcGggVEQKICAgIHN1YmdyYXBoIFByb2FjdGl2ZSBNZWNoYW5pc21zCiAgICBDW0Nyb24gSm9iIEVuZ2luZV0gLS0+fEZpeGVkIFRpbWV8IFRbVHJpZ2dlciBBZ2VudF0KICAgIEhbSGVhcnRiZWF0IExvb3BdIC0tPnxFdmVyeSA1IG1pbnN8IEV7RXZhbHVhdGUgU3RhdGV9CiAgICBFIC0tPnxJZiBhY3Rpb24gbmVlZGVkfCBUCiAgICBlbmQ=)

---

## ⚡ Keeping Your Local Session Active
This is why we set up the "Always Awake" strategy in Chapter 8. 
*   **The Check**: If your computer is in "Sleep" mode at 9:00 AM, the Cron Job will fail to fire. 
*   **The Fix**: Ensure your power settings are set to **"Never Sleep"** when plugged in. This allows your agent to work for you 24/7 without needing a remote server.

---

## ✅ Automation Success Check
Try asking your agent: *"Show me my current active cron jobs."*
It should list the morning reminder we set up!

**Next Lesson:** We’ve mastered automation, now let’s look at how to scale! We’re going to discuss **Multi-Agent Architecture** for work and life!

