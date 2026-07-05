# Day 18


## What is a merge conflict?

An event where Git cannot automatically combine two branches because changes in them crash into each other. Git stops and forces you to decide which code to keep.


## Why does it happen?

It happens when two different branches modify the exact same line of the exact same file, or when one person deletes a file that another person is trying to edit. Git doesn't know which version is correct.


## What does the markers means?

<<<<<<< HEAD: Your current local version

======= Separator

>>>>>>> commit-id: Incoming version from GitHub.


## How do you resolve a conflict?

Step 1: Open the conflicted file.

Step 2: Delete the conflict markers.

Step 3: Edit the text so only correct,final code remians.

Step 4: Save the file, stage it (git add), and run git commit to finalize the merge.


## Why are conflicts common in teams?

Because multiple developers are working simultaneously on different features within the same codebase. If two people fix bugs in the same file or work on the same layout component at the same time, their changes will inevitably cross paths when merging.
