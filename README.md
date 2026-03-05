# 🎻 Orchestra Engine Local

Welcome to **Orchestra Engine Local**, your personal automation hub for creating high-quality content using structured blueprints and powerful skills.

## 🚀 Getting Started

Follow these simple steps to get your local orchestra up and running:

1.  **Clone the Repository**
    Open your terminal and run:
    ```bash
    git clone https://github.com/Gekko-Company/orchestra-engine-local.git
    ```

2.  **Open in Antigravity**
    Launch **Antigravity** and open the `orchestra-engine-local` folder.

3.  **Command the Orchestra**
    In the Antigravity chat, type your command using the `/orch` prefix. This follows the steps described in the workflow `.agents/workflows/orch.md`, **consider this the meta-skill**.
    
    > [!IMPORTANT]
    > **Do not use Planning Mode** for these commands. Type them directly into the standard chat.

    **Example:**
    ```text
    /orch create a tweet about plant-based protein
    ```


## ✨ Available Skills

### 🔄 GitHub Sync
Keep your work in sync with the cloud effortlessly. When you've finished a task or want to save your progress, simply tell the agent:

```text
update with GitHub <explanation of what you did>
```

or

```
/github-sync <explanation of what you did>
```

Note: /output isn't synced (it's listed in .gitignore)

**What this does:**
*   Pulls the latest changes (resolving conflicts automatically).
*   Stages and commits your work with your provided explanation.
*   Pushes everything to GitHub.

---

### Update Blueprint Index 
Keeps the index in file with metadata from the blueprints.

```text
update blueprint index
```

**What this does:**
*   Scans the `blueprints` folder for new or updated blueprint files.
*   Updates the `BLUEPRINT_INDEX.md` file with the latest information.
*   Provides a summary of the changes made.



*Powered by [Antigravity](https://github.com/Gekko-Company/antigravity)*
