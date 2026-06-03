## Step 7: Resolving a Merge Conflict

You've merged branches before, and Git handled it automatically. But what happens when two branches change the **same line** in different ways? Git can't guess which version you want, so it asks **you** to decide. This is called a **merge conflict**. 😱

Don't worry, conflicts are a normal part of collaboration, and resolving them is a skill you'll use often!

### 📖 Theory: What is a Merge Conflict?

A merge conflict happens when Git tries to combine two branches that made **competing changes to the same part of a file**. Instead of picking one automatically, Git pauses the merge and marks the conflicting section so you can resolve it.

Git marks a conflict using three markers:

```diff
<<<<<<< HEAD
The change on your current branch (e.g. main)
=======
The change coming from the branch you are merging
>>>>>>> branch-name
```

To resolve a conflict, you:

1. Open the file and find the conflict markers.
1. Edit the content to the version you want (keep one side, the other, or combine them).
1. Remove the `<<<<<<<`, `=======`, and `>>>>>>>` markers.
1. Stage the file and commit to complete the merge.

### ⌨️ Activity 1: Create and resolve a conflict (using the CLI)

Let's intentionally create a conflict by editing the game's subtitle on two branches, then resolve it.

1. Make sure you are on the `main` branch with a clean working tree.

   ```bash
   git checkout main
   git status
   ```

1. Create a branch for an alternative subtitle and switch to it.

   ```bash
   git branch update-subtitle
   git checkout update-subtitle
   ```

1. Open `src/index.html`. On `line 14`, change the subtitle text, then commit.

   ```html
   <div class="subtitle">Stack the bugs before they stack up on you!</div>
   ```

   ```bash
   git add src/index.html
   git commit -m "Update subtitle to a playful message"
   ```

1. Switch back to `main` and change the **same line** to a different message, then commit.

   ```bash
   git checkout main
   ```

   ```html
   <div class="subtitle">Clear the error patterns to keep the stack stable!</div>
   ```

   ```bash
   git add src/index.html
   git commit -m "Update subtitle to a descriptive message"
   ```

1. Now merge the feature branch into `main`. Git will report a **conflict**!

   ```bash
   git merge update-subtitle
   ```

   <br/>

   ```txt
   Auto-merging src/index.html
   CONFLICT (content): Merge conflict in src/index.html
   Automatic merge failed; fix conflicts and then commit the result.
   ```

1. Check the status to confirm the conflict.

   ```bash
   git status
   ```

1. Open `src/index.html` and find the conflict markers around `line 14`. Edit the section to keep just **one** subtitle (your choice), and **delete all three** conflict markers. For example:

   ```html
   <div class="subtitle">Clear the error patterns to keep the stack stable!</div>
   ```

1. Stage the resolved file and commit to finish the merge. Make sure your commit message mentions the **conflict**.

   ```bash
   git add src/index.html
   git commit -m "Resolve merge conflict in game subtitle"
   ```

1. With the conflict resolved, Mona should already be busy checking your work. Give her a moment and keep watch in the comments. You will see her respond with progress info and the next steps.

### ⌨️ Activity 2 (optional): Resolve a conflict (using VS Code)

VS Code includes a friendly visual editor for conflicts.

1. When a conflict occurs, open the conflicted file from the **Source Control** tab.

1. VS Code highlights the conflicting region and shows action links above it:

   - **Accept Current Change** - keep the version on your branch (`HEAD`).
   - **Accept Incoming Change** - keep the version from the merging branch.
   - **Accept Both Changes** - keep both, one after the other.
   - **Compare Changes** - open a side-by-side merge editor.

   <br/>

1. Choose an option (or edit manually), then stage and commit the file from the **Source Control** tab to complete the merge.

> [!TIP]
> Always review the file after resolving! Accepting a change is quick, but you still want to make sure the final result makes sense.

<details>
<summary>Having trouble? 🤷</summary><br/>

- If you get stuck mid-merge and want to start over, you can cancel it with `git merge --abort` and try again.
- Make sure you removed **every** conflict marker (`<<<<<<<`, `=======`, `>>>>>>>`). Git won't let you commit a clean resolution if they remain.
- Your final commit message must contain the word **conflict** for Mona to mark this step complete.

</details>
