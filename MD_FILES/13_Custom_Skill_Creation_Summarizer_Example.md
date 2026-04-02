# 13 Custom Skill Creation (Summarizer Example)

You’ve used the built-in skills, but what if you want OpenClaw to do something **unique to your workflow**? That’s where **Custom Skills** come in. In this chapter, we’re going to walk through the anatomy of a skill by looking at a "Summarizer" example.

---

## 🐍 Why Write Custom Skills?
*   **Unique APIs**: Connect to your company’s internal tools.
*   **Custom Logic**: Perform complex tasks (like processing images or data) before the AI sees them.
*   **Ownership**: You have full control over the code your assistant runs.

---

## 🏗️ The Anatomy of a Custom Skill
A skill is just a simple Python file. Here is the basic structure:

```python
# FILE: summarize.py
from openclaw import skill

@skill(
    name="summarize_text",
    description="Summarizes a long piece of text into three bullet points."
)
def summarize(text: str) -> str:
    # Your custom logic here
    # (In a real skill, you might call another API or use a local library)
    summary = f"Summary: {text[:100]}..."
    return summary
```

### 🧠 The Skill Lifecycle
1.  **Define**: Create the Python file.
2.  **Decorate**: Use `@skill` to tell OpenClaw what it does.
3.  **Deploy**: Save it in the skills folder.
4.  **Register**: The Agent automatically "sees" it and adds it to its toolbox.

---

## 📍 Where Do Custom Skills Live?
You can find (and add) custom skills in this directory:
*   **Mac**: `~/.openclaw/workspace/skills/`
*   **Windows**: `C:\Users\<YourUser>\.openclaw\workspace\skills\`

---

## 🔄 Custom Skill Visualization
Here is the step-by-step logic the agent uses when it triggers your new skill:


``

``

![Diagram](https://mermaid.ink/img/Zmxvd2NoYXJ0IExSCiAgICBTdGFydFtEZWZpbmUgQHNraWxsIHdyYXBwZXJdIC0tPiBBcmdzW0RlZmluZSBhcmd1bWVudHMvc2NoZW1hXQogICAgQXJncyAtLT4gTG9naWNbSW1wbGVtZW50IFN1bW1hcml6YXRpb24gTG9naWNdCiAgICBMb2dpYyAtLT4gUmV0dXJuW1JldHVybiBzdHJpY3RseSBmb3JtYXR0ZWQgdGV4dF0KICAgIFJldHVybiAtLT4gUmVnaXN0ZXJbUmVnaXN0ZXIgc2tpbGwgaW4gQWdlbnQgQ29uZmlnXQ==)

---

## ✅ Custom Skill Success Check
After adding a new `.py` file to the skills folder, restart your OpenClaw session and ask: *"Can you use the 'summarize_text' skill?"*
Your agent should recognize it and be ready to use it!

**Next Lesson:** Let’s connect your agent to the live internet using one of the most popular skills—**Tavily Web Search**.

