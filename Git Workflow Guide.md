# Git Workflow Guide

### 1. Git Commands

- **`git pull`**  
  To fetch and merge the latest changes from the remote repository.

- **`git branch <tag/ticket#_shortdescription_initial>`**  
  Create your own branch to isolate your work.

- **`git checkout <tag/ticket#_shortdescription_initial>`**  
  Switch to your newly created branch before making any changes to avoid accidental pushes to protected branches.

- **`git add * .`**  
  Add all modified and new files to the staging area.

- **`git commit -m “<short description>”`**  
  Commit your staged changes with a short, descriptive message.

- **`git push -u origin <branch name>`**  
  Push your committed changes to the remote repository.

---

### 2. Branch Naming Convention

- **Main Branches:**
  - `master` or `main`: The main production-ready branch.
  - `staging`: Pre-release branch for integration testing.
  - `develop`: Active development branch.

- **Feature Branch:**
  - `feature/{ticket#}_shortdescription_initial`

- **Fixes Branch:**
  - `fix/{ticket#}_shortdescription_initial`

- **Hotfix Branch:**
  - `hotfix/{ticket#}_shortdescription_initial`

---

### 3. Commit Message Guidelines

**Commit messages consist of four parts:**
1. **Tag**
2. **Module**
3. **Short Description**
4. **Full Description**

**Format:**

```
[TAG] module: Short description (< 50 characters)

Full description of the change. Explain WHY the change was made, including any relevant context or rationale for the decision. Provide details about the feature being introduced, technical decisions made, or specific bugs fixed.

References:
task-123 (related to task)
Fixes #123 (closes related issue on GitHub)
Closes #123 (closes related PR on GitHub)
opw-123 (related to ticket)
```

**Commit Message Rules:**
- Separate subject from the body with a blank line.
- Limit the subject line to 50 characters.
- Capitalize the subject line.
- Do not end the subject line with a period.
- Use imperative mood in the subject line (e.g., "Add feature").
- Wrap the body at 72 characters.
- Explain **WHY** the change was made, focusing on reasons behind the change rather than simply describing what was changed.

**Example:**

```
[TAG] module: Short description of the change

This commit addresses the issue where _________. The previous behavior resulted in ________. The new implementation does _________ because of ________.
```

---

### 4. Tags for Commit Messages

| Tag  | Description |
| ---- | ----------- |
| `[FIX]`  | For bug fixes, primarily in stable versions but also for recent bugs in development. |
| `[REF]`  | For refactoring, when a feature is heavily rewritten. |
| `[ADD]`  | For adding new modules. |
| `[REM]`  | For removing resources like dead code, views, or modules. |
| `[REV]`  | For reverting commits that caused issues or are no longer wanted. |
| `[MOV]`  | For moving files or code across files. |
| `[REL]`  | For release commits (new major or minor stable versions). |
| `[IMP]`  | For incremental improvements in the development version. |
| `[MERGE]`| For merge commits, often used for forward-porting bug fixes or when several commits are involved in a feature. |
| `[CLA]`  | For signing the Odoo Individual Contributor License. |
| `[I18N]` | For changes in translation files. |

**Module Naming:**  
Use the technical module name in your commits (e.g., `sale`, `account`). If multiple modules are modified, list them, or use "various" for cross-module changes.

---

### 5. Git Commit Format

**Format:**
```
[Tag] module_folder: Short description

Ticket #123 As a <User>, I want to _______, so that _______.
```