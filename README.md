# Second Year Task 1 — Drone Club

Welcome to the **Drone Club** initial task for second-year students of **AKGEC**!

This task is a hands-on introduction to the Git and GitHub workflow that we use for every project in the club. By the end, you will have forked a repo, worked on a branch, committed a file, and raised your first Pull Request.

---

## Repository Structure

```
.
├── second_year/     # Second-year students add their JSON file here
├── third_year/      # Reserved for third-year students (do not touch)
└── README.md
```

---

## The Task

Create **one JSON file** inside the `second_year/` folder with your details, and submit it via a Pull Request.

### File name rules

- The file name must be **your name** followed by `.json`
- It may contain **only letters and underscores** (no spaces, digits, hyphens or other special characters)
- Use an underscore in place of the space between your first and last name

| Valid | Invalid |
| --- | --- |
| `jane_doe.json` | `jane doe.json` (space) |
| `rahul_kumar_sharma.json` | `rahul-sharma.json` (hyphen) |
| `priya.json` | `priya123.json` (digits) |

### File content format

```json
{
  "name": "jane doe",
  "branch": "<your B.Tech branch>",
  "domain": ["<domain 1>", "<domain 2>"],
  "quote": "<any quote you like>"
}
```

| Field | Type | Description |
| --- | --- | --- |
| `name` | string | Your full name |
| `branch` | string | Your B.Tech branch (e.g. `CSE`, `CSE-AIML`, `IT`, `ECE`, `EE`, `ME`) |
| `domain` | array of strings | All the domains you are part of in the club |
| `quote` | string | Any quote you like |

### Example: `second_year/jane_doe.json`

```json
{
  "name": "jane doe",
  "branch": "CSE",
  "domain": ["Programming", "Fabrication"],
  "quote": "Talk is cheap. Show me the code."
}
```

---

## Step-by-Step Guide

### Step 1: Fork the repository

1. Click the **Fork** button at the top-right of this repository's page.
2. Select your own GitHub account as the destination.

This creates a copy of the repo under your profile.

### Step 2: Clone your fork to your PC

```bash
git clone https://github.com/<your-github-username>/<repo-name>.git
cd <repo-name>
```

### Step 3: Create a new branch for development

Never work directly on `main`. Create a branch named after yourself:

```bash
git checkout -b add-<your_name>
```

Example:

```bash
git checkout -b add-jane_doe
```

### Step 4: Create your JSON file

Create a file inside the `second_year/` folder named `<your_name>.json` (following the naming rules above) and fill in your details.

```bash
# Linux / macOS
touch second_year/jane_doe.json

# Windows (PowerShell)
New-Item second_year/jane_doe.json
```

Open it in any editor and paste in the JSON format with your own details.

### Step 5: Add the file

```bash
git add second_year/jane_doe.json
```

Run `git status` to confirm that only your file is staged.

### Step 6: Commit your changes

```bash
git commit -m "Add jane_doe.json"
```

### Step 7: Push your changes

Push your branch to your fork:

```bash
git push origin add-jane_doe
```

### Step 8: Open a Pull Request

1. Go to **your fork** on GitHub.
2. You will see a banner saying *"Compare & pull request"*. Click it. If it is missing, go to the **Pull requests** tab → **New pull request**.
3. Make sure the PR is set up as:
   - **base repository:** the original club repo
   - **base branch:** `main`
   - **head repository:** your fork
   - **compare branch:** `add-<your_name>`
4. Give the PR a clear title, for example: `Add jane_doe.json`
5. Click **Create pull request**

---

## Submission Checklist

Before you raise your PR, make sure that:

- [ ] Your file is inside the `second_year/` folder
- [ ] The file name contains only letters and underscores and ends with `.json`
- [ ] The JSON is valid and follows the exact format given above
- [ ] `domain` is an array (e.g. `["Web Dev"]`), even if you have only one domain
- [ ] Your PR contains **only one new file**: yours
- [ ] You have not modified any other files or the `third_year/` folder

---

## In case of queries?

Don't worry, everyone struggles with Git at first. Reach out to your seniors or ask in the club's group chat, and we'll help you out.

**Happy committing!**
