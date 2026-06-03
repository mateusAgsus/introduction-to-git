## Step 6: Tracking Work with Issues

Our game is coming along nicely! But as a project grows, you need a way to keep track of bugs, ideas, and tasks, so nothing gets forgotten. This is especially important when collaborating with others.

This is where **issues** come in. 🗒️

### 📖 Theory: What are Issues?

An **issue** is a way to track work directly inside your repository on GitHub. Think of it as a to-do item, bug report, or discussion thread tied to your project.

Issues are great for:

- **Reporting bugs**: Describe something that isn't working as expected.
- **Planning features**: Capture an idea before you start coding.
- **Organizing work**: Break a big goal into smaller, trackable tasks.
- **Collaborating**: Discuss the work with teammates in one place.

To keep things organized, an issue can include:

- **Title**: A short, clear summary of the work.
- **Description**: The details, context, and steps to reproduce (for bugs).
- **Labels**: Tags like `bug`, `enhancement`, or `documentation`.
- **Assignees**: The people responsible for the work.
- **Milestones**: A group of issues working toward a larger goal.

> [!TIP]
> A good issue title is specific. "Bug" is hard to act on, but "High score resets when the page is refreshed" tells everyone exactly what to look at.

### ⌨️ Activity 1: Create an issue (using the web browser)

While building the game, you noticed the high score doesn't always behave as expected. Let's track that with an issue!

> [!IMPORTANT]
> Create this issue on **your copy** of the exercise repository, not on the tracking issue Mona is using for this exercise.

1. In a new browser tab, open the **Issues** tab of your repository.

   [Open the Issues tab →](../../issues)

1. Click the green **New issue** button.

1. Give your issue a clear, specific **title**.

   ```txt
   Bug: high score is lost after refreshing the page
   ```

1. Add a **description** with some helpful details.

   ```md
   ## What happens
   The high score resets to 0 every time the page is reloaded.

   ## Expected behavior
   The high score should persist between sessions.

   ## Notes
   Likely related to how we read and write the value in localStorage.
   ```

1. Click **Submit new issue** to create it.

1. With your issue created, Mona should already be busy checking your work. Give her a moment and keep watch in the comments. You will see her respond with progress info and the next steps.

### ⌨️ Activity 2: Create an issue (using the CLI)

You can also create issues without leaving your editor, using the [GitHub CLI](https://cli.github.com/) (`gh`) in the integrated terminal.

1. In the terminal, create an issue with a single command.

   ```bash
   gh issue create --title "Add a restart button" --body "Players should be able to restart the game without reloading the page."
   ```

   > 🪧 **Note**: The first time you use `gh`, it may ask you to authenticate. Follow the on-screen prompts.

1. List the issues in your repository to confirm it was created.

   ```bash
   gh issue list
   ```

> [!TIP]
> You can close an issue from the CLI too, once the work is done: `gh issue close <number>`.

<details>
<summary>Having trouble? 🤷</summary><br/>

- Make sure you are creating the issue on **your** copy of the repository, not the original `skills/introduction-to-git`.
- An issue needs both a **title** and a **description** for Mona to mark this step complete.

</details>
