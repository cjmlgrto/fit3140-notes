[← Return to Index](https://github.com/cjmlgrto/fit3140-notes/)

# Version Control

- Software changes a lot, and many multiple different versions can accumulate quickly (sometimes, even lost) if it isn't managed correctly and efficiently. 
- Another problem is when more than one person is working on a single file: changes can be incorrectly merged (or worse, possibly overwritten and ignored).
- **Version Control** solves this.

## Version Control Systems

### Key Features

- automates the process of tracking revisions
- supports multiple authors
- allows the retrieval of previous versions
- stores changes in a space-efficient way
- and makes keeping track of important _branches_ (alternate versions of the same copy) easy

**Git** is a popular open-source version control system that is _distributed_ (you keep full version history locally). **GitHub** is an online service that can keep a copy of your git repository remotely. (Another altnernative is **Bitbucket**).

## Managing Simultaneous Access

### The Problem

1. Two users read the same file
2. They both begin to edit their copies
3. User A publishes their version first
4. User B accidentally overwrites User A's version (because User B doest not have any of User A's changes)

### The Locking Solution

1. User A locks the file then copies it for editing
2. While User A edits, User B attempts to lock but it fails
3. User A publishes their version, then releases the lock
4. User B can now lock and edit the latest version

### The Git Solution

1. Two users copy the same file
2. They both begin to edit their copies
3. User A compares the latest version to their own
4. A new merged version is created
5. User B publishes their version first
6. User A gets an "out of date" error
7. User A fetches the changes from the new version and merges
8. User A then publishes their version
9. User B then gets an "out of date" error
10. User B then fetches & mergest the changes from the newer version
11. Both users now have each other's changes

## Branching and Merging

- **Branch** — a parallel development path
- **Merge** — occurs when two branches are combined
- **Trunk or Master** — the base version where all development takes place

### Typical Daily Workflow

1. Update _working copy_
2. Edit working copy
3. Possibly _pull changes_ during the day, to incorporate others' changes
4. _Commit and push changes_, resolving conflicts if necessary

