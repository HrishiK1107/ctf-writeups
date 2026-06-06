# Bandit Level 29 → Level 30

**Concept:** Git Branch Enumeration

**Difficulty:** Trivial

## What the level asks

A Git repository is available through SSH. The objective is to identify information stored outside the default branch and locate the password for the next Bandit level.

## Approach

After cloning the repository, the contents of the default branch were reviewed. The visible files did not contain the required password, suggesting that additional information might exist elsewhere within the repository.

To identify alternative development paths, all local and remote branches were enumerated. This revealed additional remote branches that were not checked out by default.

One of the development branches contained additional project files and documentation. After switching to the branch and reviewing the repository contents, the password for the next level was located within the branch-specific data.

## Solution

```bash
git clone ssh://bandit29-git@bandit.labs.overthewire.org:2220/home/bandit29-git/repo

cd repo

cat README.md

git branch -a

git checkout remotes/origin/dev

cat README.md

# Password obtained:
# [REDACTED]
```

### Screenshot

![Git Branch Enumeration](assets/git-branch-enumeration.png)

**Caption:** Enumerating repository branches and inspecting an alternate development branch.

**Explanation:** The screenshot shows discovery of additional branches within the repository, checkout of a development branch, and retrieval of information that was not present on the default branch.

## Real-World Relevance

Development teams commonly use multiple branches for feature development, testing, staging, and release management. Security professionals frequently inspect non-default branches because sensitive information, unfinished features, configuration changes, and exposed credentials may exist outside the primary codebase while still remaining accessible through version control.
