📌 Day 4: GitHub & Git Workflow – Pull Requests, Conflicts & Collaboration
🔹 Topics Covered:
✔ GitHub Workflow – Fork, Clone, Branch, PR
✔ Creating & Merging Pull Requests (PRs)
✔ Handling Merge Conflicts
✔ Best Practices for Collaboration

1️⃣ GitHub Workflow
A standard GitHub workflow for collaboration:

Clone the repo (if not already cloned):

bash
Copy
Edit
git clone <repo_url>
cd <repo_name>
Create a new branch for your feature/work:

bash
Copy
Edit
git checkout -b feature-branch
Make changes, then stage & commit:

bash
Copy
Edit
git add .
git commit -m "Added new feature"
Push changes & create a Pull Request (PR):

bash
Copy
Edit
git push origin feature-branch
Submit PR on GitHub, request a review, and merge.

2️⃣ Merging & Resolving Conflicts
When merging branches, conflicts may occur if the same file is modified in both branches.

To resolve a merge conflict:

Open the conflicted file.

Look for conflict markers (<<<<<<<, =======, >>>>>>>).

Manually edit the file to keep the correct changes.

Stage & commit the resolved file:

bash
Copy
Edit
git add <file>
git commit -m "Resolved merge conflict"
Push the updated branch and complete the merge.

3️⃣ Best Practices for GitHub Collaboration
✔ Always work in a feature branch, never directly on main.
✔ Keep PRs small and focused to ease the review process.
✔ Use meaningful commit messages to track changes effectively.
✔ Regularly pull the latest changes to avoid conflicts.
✔ Always review PRs before merging to ensure quality.
