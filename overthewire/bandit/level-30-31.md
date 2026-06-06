# Bandit Level 30 → Level 31

**Concept:** Git Tag Enumeration

**Difficulty:** Trivial

## What the level asks

A Git repository is provided through SSH. The objective is to inspect the repository and identify information stored outside the normal branch and commit structure.

## Approach

After cloning the repository, the contents of the default branch were inspected. The repository contained only a README file, which intentionally provided no useful information.

Since previous Git challenges had hidden information within repository metadata, additional Git objects were enumerated. Branch enumeration revealed no unusual content, but inspection of repository tags identified a tag named `secret`.

The contents associated with the tag were displayed using Git's object inspection functionality. The tag contained the password required for the next Bandit level.

## Solution

```bash
git clone ssh://bandit30-git@bandit.labs.overthewire.org:2220/home/bandit30-git/repo

cd repo

cat README.md

git branch -a

git tag

git show secret

# Password obtained:
# [REDACTED]
```

### Screenshot

![Git Tag Discovery](assets/git-tag-discovery.png)

**Caption:** Enumerating Git tags to identify hidden repository data.

**Explanation:** The screenshot demonstrates discovery of a repository tag named `secret` and inspection of its contents, revealing information that was not accessible through the normal branch structure.

## Real-World Relevance

Git repositories contain more than files and branches. Tags are frequently used to mark releases, milestones, and important repository states. Security assessments often include inspection of tags because historical data, credentials, deployment information, or development artifacts may remain accessible through repository metadata even when they are not visible within active branches.
