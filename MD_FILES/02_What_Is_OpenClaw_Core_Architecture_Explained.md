# 02 What Is OpenClaw? Core Architecture Explained

Now that we’ve seen the "Why," let’s look at the "How." 

Think of OpenClaw as a super-powered digital brain that can control different apps and services for you. But to truly master it, you need to understand its **Four Core Pillars**. Let’s break them down simply.

---

## 🏗️ The Four Pillars of OpenClaw

### 1. The Chat Channel (Your Interface)
This is where you talk to your agent. It’s the user interface you use every day. OpenClaw supports everything from:
*   **Web UI**: A clean, dashboard-like interface in your browser.
*   **Telegram / WhatsApp**: Chatting with your bot just like you chat with a friend.
*   **TUI (Terminal User Interface)**: For those who love the command line and want deep control.

### 2. The OpenClaw Gateway (The Mailman)
The Gateway is like the post office. When you send a message on Telegram, it doesn't go straight to the AI. First, it hits the **Gateway**. The Gateway receives your message, processes it, and then hands it over to the Agent. It also ensures that when the Agent has an answer, it gets sent back to the right channel.

### 3. The Agent (The Brain)
This is the heart of the system. In this course, we’re mostly using **Gemini 2.5 Flash** as the brain. The Agent receives your message from the Gateway, decides what needs to be done, and figures out which "Skills" it needs to use to complete the task.

### 4. Skills & MCP (The Hands)
This is what makes OpenClaw better than a simple chatbot. **Skills** are pieces of code (often based on the Model Context Protocol or MCP) that allow the Agent to actually *do things*. 
*   Want to summarize an email? Use an **Email Skill**.
*   Want to check the weather? Use a **Weather Skill**.
*   Want to search the web? Use a **Tavily Search Skill**.

---

## 🔄 The Communication Flow
Here's a visual look at how these pillars talk to each other. When you send a message, it travels through this exact loop:


``

``

![Diagram](https://mermaid.ink/img/Zmxvd2NoYXJ0IExSCiAgICBVc2VyKFtVc2VyXSkgPC0tPiBHYXRld2F5W0NvcmUgR2F0ZXdheV0KICAgIEdhdGV3YXkgPC0tPiBBZ2VudHtBZ2VudCBDb3JlfQogICAgQWdlbnQgPC0tPiBNZW1vcnlbKE1lbW9yeSAvIFNvdWwpXQogICAgQWdlbnQgLS0+IFNraWxsc1tTa2lsbHMgJiBUb29sc10KICAgIFNraWxscyAtLT4gV2ViW1dlYiBTZWFyY2hdCiAgICBTa2lsbHMgLS0+IExvY2FsW0xvY2FsIFNjcmlwdHNd)

---

## 🧠 Memory: The "Soul" and "Identity" Files
OpenClaw doesn't just forget everything after one session. It stores information in two very important Markdown files:
*   **`identity.md`**: This defines *who* the agent is (e.g., "I am your helpful assistant, Jarvis").
*   **`soul.md`**: This defines *how* the agent behaves and what it cares about.

By editing these files (which the agent can even do itself!), your assistant develops a personality that evolves based on your interactions.

**Next Up:** We'll explore the real-world use cases and what you can actually build!

