# The Core Purpose of Branching

- Parallel Development: This is the fundamental concept. Branches allow multiple features (e.g., a new UI, a backend optimization, a bug fix) to be developed concurrently by different individuals or teams. Without branching, developers would be constantly stepping on each other's code.
- Context Switching and Experimentation: A branch is a safe sandbox. You can try a radical new algorithm or refactor a module. If it doesn't work, you simply discard the branch (git branch -D experiment_branch) and no harm is done to the main codebase. This encourages innovation and reduces risk.
- Synching Vs Asynching:
- - Head: A pointer to a specific commit (a snapshot of your code).
- - Syncing: This means the branches point to the exact same commit, meaning their history is identical at that point.
- - Behind/Ahead: This describes the state of a branch's history relative to another branch.
    icecream is one commit behind master means the commit that icecream points to is a direct parent of the commit that master points to. To "sync" them, you would need to bring the changes from master into icecream **(usually with a merge or rebase)**.
