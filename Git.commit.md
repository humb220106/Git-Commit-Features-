**Different Features of Git Commit with Explanations and Examples**

### 1. **Message Description**
Every commit has a message that describes the changes made. Commit messages help you and your team understand the purpose of each change.

**Example:**
```sh
git commit -m "Refactored login feature for better performance"

git commit -m "feat: add dark mode toggle in user settings"

git commit -m "fix: resolve issue with form validation not triggering on submit"

git commit -m "docs: update API usage examples in README"

git commit -m "style: fix indentation and remove trailing spaces in main.css"

git commit -m "refactor: rename 'userData' to 'userProfile' for better clarity"

git commit -m "test: add unit tests for authentication middleware"

git commit -m "chore: update eslint config to enforce new style rules"

```
---

### 2. **Amend Previous Commit**
Modify the most recent commit. If you forgot to add files or want to correct the commit message, you can amend the last commit.

**Example:**
```sh
git commit --amend -m "Updated login feature with optimized query"

git commit --amend -m "fix: correct typo in error message"

```

---

### 3. **Staging Partial Changes**
Commit only selected changes in a file. You can stage and commit specific parts of a file instead of committing the entire file.

**Example:**
```sh
git add -p
git commit -m "Fixed typo in README.md"

git add -p  
git commit -m "fix: correct calculation error in order total"

```

---

### 4. **Sign-Off (Verified Commits)**
Add a sign-off to your commit. Used in projects that require contributors to certify their work (e.g., Developer Certificate of Origin).

**Example:**
```sh
git commit -s -m "Added authentication middleware"

git commit -s -m "feat: implement JWT authentication"

git commit -s -m "feat(security): add role-based access control"


```

---

### 5. **Committing with Author Identity**
Commit changes as a specific author. Useful when multiple contributors work on a shared machine or during code reviews.

**Example:**
```sh
git commit --author="Alex Smith <alex.smith@example.com>" -m "Updated API response structure"

git commit --author="Alice Doe <alice@example.com>" -m "fix: correct date formatting in reports"

```

---

### 6. **Empty Commits**
Create commits with no file changes. Useful for testing or marking a point in history without modifying files.

**Example:**
```sh
git commit --allow-empty -m "Triggering CI/CD pipeline"

git commit --allow-empty -m "chore(ci): trigger deployment pipeline"


```

---

### 7. **Squashing Commits**
Combine multiple commits into one. Makes your commit history cleaner by consolidating changes.

**Example:**
```sh
git rebase -i HEAD~4

git rebase -i HEAD~3  # Choose "squash" (s) for unwanted commits  

```

---

### 8. **Interactive Rebase**
Modify, reorder, or squash previous commits. Allows you to refine your commit history before sharing it with others.

**Example:**
```sh
git rebase -i HEAD~6

git rebase -i HEAD~5

```

---

### 9. **Diff Viewing Before Commit**
View changes before committing. Helps verify changes before finalizing the commit.

**Example:**
```sh
git diff --staged

git add -p  
git commit -m "fix: correct calculation error in order total"

```

---

### 10. **GPG-Signed Commits**
Sign commits with a GPG key. Ensures the authenticity of the commit and proves it was made by you.

**Example:**
```sh
git commit -S -m "Implemented OAuth security layer"

git commit -s -m "feat: implement JWT authentication"

```

---

### 11. **Commit Templates**
Use a predefined template for commit messages. Helps enforce a consistent message format.

**Example:**
```sh
git config commit.template ~/.gitmessage.txt
git commit

git commit --author="Alice Doe <alice@example.com>" -m "fix: correct date formatting in reports"

```

---

### 12. **Skipping Hooks**
Bypass Git hooks during commit. Use this if you want to skip pre-commit checks for specific commits.

**Example:**
```sh
git commit --no-verify -m "Quick patch for deployment issue"

git commit --no-verify -m "fix: hotfix for production issue"

```

---

### 13. **Commits with Date Specification**
Set a custom commit date. Useful for backdating commits or when you forgot to commit earlier.

**Example:**
```sh
GIT_AUTHOR_DATE="2025-03-01T10:15:00" GIT_COMMITTER_DATE="2025-03-01T10:15:00" git commit -m "Backdated security fix"

GIT_AUTHOR_DATE="2025-03-01T10:15:00" GIT_COMMITTER_DATE="2025-03-01T10:15:00" git commit -m "fix: backdated security patch"

```

---

### 14. **Verbose Commit**
Show detailed changes in the commit message editor.

**Example:**
```sh
git commit --verbose
```

---

### 15. **Dry Run Commit**
Simulate a commit without actually making it.

**Example:**
```sh
git commit --dry-run
```

---

### 16. **Committing Using a Template File**
Use a custom commit message template from a file.

**Example:**
```sh
git commit -t commit-template.txt

git commit -S -m "feat(security): implement end-to-end encryption"

```

---

### 17. **Using a Global Commit Template**
Set a global commit template for consistency.

**Example:**
```sh
git config --global commit.template ~/.git-commit-template.txt


```

---

### 18. **Commit Tree**
Create a commit from an existing tree object without modifying the working directory.

**Example:**
```sh
git commit-tree HEAD^{tree} -m "Recreated commit for consistency"

git commit-tree HEAD^{tree} -m "chore: recreate commit for consistency"

git commit-tree HEAD^{tree} -m "chore(repo): restructure project files"


```

---

### 19. **Soft Reset Commit**
Undo the last commit but keep changes staged.

**Example:**
```sh
git reset --soft HEAD~1

git reset --soft HEAD~1
git commit -m "fix(build): correct missing dependency import"


```

---

### 20. **Hard Reset Commit**
Completely remove the last commit and its changes.

**Example:**
```sh
git reset --hard HEAD~1
```

---

### 21. **Fixing a Specific Commit**
Create a fixup commit to be automatically squashed later.

**Example:**
```sh
git commit --fixup=<commit-hash>
```

---

### 22. **Autosquash Fixup Commits**
Automatically squash fixup commits when rebasing.

**Example:**
```sh
git rebase -i --autosquash HEAD~5
```

---

### 23. **Editing a Specific Commit**
Modify an older commit without affecting newer ones.

**Example:**
```sh
git rebase -i HEAD~4
```

---

### 24. **Reset Last Commit Message**
Reset the author information on the last commit.

**Example:**
```sh
git commit --amend --reset-author
```

---

### 25. **Adding a Co-Author**
Include multiple authors in a commit.

**Example:**
```sh
git commit -m "Implemented new feature" --author="John Doe <john@example.com>"

git commit -m "feat: add image cropping feature" --author="John Doe <john@example.com>"

```

---