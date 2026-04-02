# 05 Local Installation (Mac and Windows)

It’s time to stop the theory and start the installation! In this chapter, we’re going to install OpenClaw on your local machine. Whether you’re on a Mac or Windows, the process is designed to be as smooth as possible—often requiring just a single command.

---

## 🛠️ Step 1: The Installation Command

The OpenClaw team has made this incredibly easy with a dedicated install script. 

### For Mac & Linux (and Windows Terminal with Bash)
Open your terminal and run:

```bash
curl -fsSL https://openclaw.ai/install.sh | sh
```

### For Windows (PowerShell)
If you prefer using native PowerShell, you can use:

```powershell
powershell -c "irm https://openclaw.ai/install.ps1 | iex"
```

> [!TIP]
> **Windows Users**: I highly recommend downloading the **Windows Terminal** app from the Microsoft Store. It handles the formatting and icons much better than the old CMD window.

---

## 📦 Dependencies & Requirements
Before the script finishes, it will check if you have the following installed:
1.  **NodeJS**: The engine that runs the OpenClaw Gateway.
2.  **Homebrew (Mac)**: Used for managing packages.
3.  **Git**: To fetch the latest OpenClaw updates.

If the script fails, don't panic! It will usually tell you exactly what is missing. Just copy the error into ChatGPT or Claude, and it will give you the one-line fix.

---

## ⚠️ The "Fire" Warning (Security)
During the installation, you will see a serious-looking warning on your screen. It will tell you:
> "OpenClaw is a hobby project... if hacked, it can have lots of repercussions."

**Why?** Because OpenClaw runs on your local machine and has access to your files and terminal. If you aren't comfortable with basic security, you need to be careful. As the video says: *"Let's select 'Yes' because we can play with fire!"* 

Just remember: **Never share your API keys or session tokens with anyone.**

---

## 🗺️ Installation Flow
Here’s what’s happening behind the scenes when you run that install command:


``

``

![Diagram](https://mermaid.ink/img/Z3JhcGggVEQKICAgIFN0YXJ0W1N0YXJ0IExvY2FsIFNldHVwXSAtLT4gQ2xvbmVbZ2l0IGNsb25lIHJlcG9dCiAgICBDbG9uZSAtLT4gVmVudltweXRob24gLW0gdmVudiB2ZW52XQogICAgVmVudiAtLT4gQWN0W0FjdGl2YXRlIHZlbnZdCiAgICBBY3QgLS0+IFJlcVtwaXAgaW5zdGFsbCAtciByZXF1aXJlbWVudHMudHh0XQogICAgUmVxIC0tPiBSdW5bcHl0aG9uIG1haW4ucHld)

---

## ✅ Success Check
Once the installation is complete, your terminal should look clean, and you might see a message about "Missing APIs." That’s perfectly normal—we haven’t given our agent a brain yet.

**Next Step:** Let's get those API keys and choose the right "brain" for your assistant!

