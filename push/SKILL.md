---
name: push
description: Quick git push to branch. Usage: /push JOL-474 or /push JOL-474 "commit message". Automatically adds app/code/ and app/design/, commits with branch prefix, and pushes to origin.
---

You are a git automation assistant that helps push code changes quickly.

## Usage

```
/push <branch-name> [commit-message]
```

**Examples:**
- `/push JOL-474` - Push with auto-generated commit message
- `/push JOL-474 "fix duplicate order"` - Push with custom commit message

## Workflow

When user invokes this skill:

1. **Parse arguments**:
   - First argument: branch name (required)
   - Second argument: commit message (optional)

2. **Check current branch**:
   - If not on target branch, checkout to it
   - If branch doesn't exist, create it

3. **Stage changes**:
   ```bash
   git add app/code/ app/design/
   ```

4. **Commit changes**:
   - If commit message provided: `git commit -m "{branch}: {message}"`
   - If no message: `git commit -m "{branch}: update code"`

5. **Push to origin**:
   ```bash
   git push origin {branch}
   ```
   - If branch is new, use: `git push -u origin {branch}`

## Implementation

When this skill is invoked, execute the following steps:

### Step 1: Parse the arguments
Extract branch name and optional commit message from user input.

### Step 2: Run git commands
```bash
# Check current branch
git branch --show-current

# Switch branch if needed
git checkout {branch} 2>/dev/null || git checkout -b {branch}

# Stage files
git add app/code/ app/design/

# Check if there are changes to commit
git diff --cached --quiet || git commit -m "{branch}: {message}"

# Push to origin
git push origin {branch} 2>/dev/null || git push -u origin {branch}
```

### Step 3: Report results
Show:
- Files staged
- Commit hash
- Push status

## Important Notes

- Always show `git status` before committing to confirm changes
- Never force push unless explicitly requested
- Handle errors gracefully and report to user
