### **Git Merge Conflicts**

#### **1. What is a Merge Conflict?**

A merge conflict is an event that occurs when Git cannot automatically reconcile the changes from two different branches. It is not an error or a failure of Git; it is a **logical inevitability** when concurrent, incompatible changes are made to the same parts of a file.

Git's automatic merging is excellent for combining changes that don't touch the same lines (e.g., you change function `A` and I change function `B`). A conflict arises when this is not the case.

#### **2. When Do Conflicts Happen?**

Conflicts occur during operations that combine history:

- `git merge`
- `git rebase`
- `git cherry-pick`
- `git pull` (which is essentially `fetch` + `merge`)

#### **3. The Root Cause: Divergent Changes**

A conflict requires **two** conditions to be true simultaneously:

1.  **The same file** was changed in both branches.
2.  **The same part(s) of that file** were changed in different ways.

**Example Scenario:**

1.  Branch `main` has a line: `favorite_ice_cream = "vanilla"`
2.  You branch off to `feature/cake` and change it to: `favorite_dessert = "chocolate cake"`
3.  Someone else on `main` changes it to: `favorite_ice_cream = "pistachio"`
4.  Attempting to merge `feature/cake` into `main` will cause a conflict. Git doesn't know which variable name (`favorite_ice_cream` vs. `favorite_dessert`) _or_ which value (`"pistachio"` vs. `"chocolate cake"`) to choose. This requires human judgment.

#### **4. Anatomy of a Conflict Marker**

When a conflict occurs, Git modifies the file in your working directory to show you the conflicting sections. It uses a specific syntax:

```python
<<<<<<< HEAD
This is the change that is currently on your branch (the one you are on).
=======
This is the change that is coming from the branch you are merging in.
>>>>>>> branch-being-merged
```

- `<<<<<<< HEAD`: Marks the **start** of the conflicting changes from your current branch.
- `=======`: The **divider** between the two conflicting sets of changes.
- `>>>>>>> branch-name`: Marks the **end** of the conflicting changes from the incoming branch.

#### **What Happens?**

Git can't automatically combine changes from two branches because they edited the same part of the same file. It asks you to decide what the final code should be.

---

#### **What You'll See in the File**

Git adds markers to show the conflict:

```python
<<<<<<< HEAD
Your changes (from your current branch)
=======
Incoming changes (from the branch you're merging)
>>>>>>> branch-name
```

- `<<<<<<< HEAD` to `=======` is **your code**.
- `=======` to `>>>>>>> branch-name` is **their code**.

---

#### **How to Fix It: 4 Steps**

1.  **Find the conflicts:**

    ```bash
    git status
    ```

    _Look for "Unmerged paths"._

2.  **Open the file** and find the `<<<<<<<` markers.

3.  **Edit the file** to choose the correct code. You can:

    - Keep only your code
    - Keep only their code
    - Mix them together
    - Write something new
    - **Delete all the conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`)**

4.  **Finish up:**
    ```bash
    git add <file>  # Mark this file as fixed
    git commit      # Finalize the merge
    ```
5.  Commit the changes

---
