# JIRA Smart Commit Helper

A simple Bash script to help you format Git commit messages with your JIRA ticket ID and project name automatically, making your commits compatible with JIRA Smart Commits.

## What does this script do?

- Extracts your project name and ticket ID from your branch name (like `feature/MYPROJECT-123-add-login`).
- Prompts you for a commit message.
- Automatically formats your commit message as:  
  `Your commit message (#MYPROJECT-123)`
- Optionally pushes your branch after committing.
- If the script can’t detect your project name, it will ask you to enter it manually.

## Why use this script?

Including the ticket ID in your commit message lets JIRA link your code changes directly to the relevant issue (using JIRA Smart Commits). This helps with traceability, makes code reviews easier, and keeps your workflow organized.

## How to use

1. Save the script (for example, as `cm` or `commit-helper.sh`) and make it executable:
    ```bash
    chmod +x cm
    ```
2. Move it to a directory in your `PATH` for global use:
    ```bash
    mv cm ~/.local/bin/cm
    ```
3. Add to PATH
    ```bash
    grep -qxF 'export PATH="$HOME/.local/bin:$PATH"' ~/.bashrc || echo 'export PATH="$HOME/.local/bin:$PATH"' >> ~/.bashrc
    ```
4. Reload shell
    ```bash
    source ~/.bashrc
    ```
5. Add changes to git:
    ```bash
    git add .
    ```
6. Run the script:
    ```bash
    cm
    ```
7. Follow the prompts for commit message and push.

## Full article and explanation

For the full story, background, and a step-by-step guide, check out my Medium post:  
👉 [Never Miss a JIRA Smart Commit: My Bash Script for Effortless Ticket Tracking](https://medium.com/your-article-link)

## License

MIT

