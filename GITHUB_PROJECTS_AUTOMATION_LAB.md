# 🎓 Instructor Guide & Student Lab: GitHub Projects Automation

## 📋 Prerequisites

* Each student (or pair) needs a **GitHub account**.
* A sample public/private repository created (e.g., `github-workflow-demo` or `c-calculator`).
* A **GitHub Project (v2)** board created and linked to the repository.

---

## Step 1: Set Up the Project Board Columns & Workflows

1. Navigate to your repository on GitHub.
2. Click the **Projects** tab $\rightarrow$ Click **New project** $\rightarrow$ Choose **Board** template $\rightarrow$ Name it **Sprint Board**.
3. Configure the board columns:
   * **Todo**
   * **In Progress**
   * **In Review**
   * **Done**
4. Open the Project Workflows menu:
   * Click the `...` (three dots menu) at the top right of the project board $\rightarrow$ Select **Workflows**.
5. Enable the following workflows:
   * ✅ **Auto-add to project** (set filter to your repo)
   * ✅ **Item added to project** (set default status to Todo)
   * ✅ **Auto-add sub-issues to project**
   * ✅ **Pull request linked to issue** (set status to In Progress)
   * ✅ **Pull request merged** (set status to Done)
   * ✅ **Auto-close issue**

---

## Step 2: Demonstrate "Auto-Add" & Default Status

1. Go back to the **Repository** page.
2. Click **Issues** $\rightarrow$ Click **New issue**.
3. Create an issue:
   * **Title**: `Issue #1: Fix header responsiveness on mobile`
   * **Submit** the issue.
4. **Student Check**: Switch to the **Projects** tab.
   * *Observation*: Notice how Issue #1 automatically appeared on the board inside the **Todo** column without any manual dragging!

---

## Step 3: Demonstrate "Sub-Issues Automation"

1. Open **Issue #1** in the repository.
2. Scroll to the **Create sub-issue** section (or task list).
3. Add a new sub-issue:
   * **Title**: `Sub-issue: Update CSS breakpoints`
4. **Student Check**: Switch back to the **Projects** board.
   * *Observation*: The sub-issue automatically appears on the project board alongside the parent issue.

---

## Step 4: Demonstrate "PR Linking & Status Change"

1. Open your terminal or GitHub web interface and create a new Pull Request.
2. Title the PR: `Fix CSS media queries`.
3. In the **PR description**, type keyword linking syntax: `Fixes #2` *(Replace #2 with the sub-issue number generated above)*
4. Submit the Pull Request.
5. **Student Check**: Look at the Project Board.
   * *Observation*: The sub-issue card automatically moved from **Todo** $\rightarrow$ **In Progress** as soon as the PR was linked.

---

## Step 5: Demonstrate "PR Merging & Auto-Done"

1. Open the created Pull Request.
2. Click **Merge pull request** $\rightarrow$ **Confirm merge**.
3. **Student Check**: Switch to the Project Board.
   * *Observation*: Both the **Pull Request** and the linked **Sub-issue** have automatically moved to the **Done** column.

---

## Step 6: Demonstrate "Board-Driven Auto-Closing"

1. Find the original parent issue (**Issue #1**) on the Project Board under **Todo**.
2. Click and drag **Issue #1** into the **Done** column.
3. **Student Check**: Open **Issue #1** on the repository Issues page.
   * *Observation*: GitHub automatically changed the state of Issue #1 from **Open** to **Closed** because it was dropped into Done.

---

## 💡 Key Takeaways for Students

* **Zero Overhead**: Developers spend less time updating project boards and more time coding.
* **Traceability**: Pull Requests explicitly track which issues they solve using standard keywords (`Fixes #ID`, `Closes #ID`).
* **Single Source of Truth**: Board status accurately reflects real git activity in real-time.
