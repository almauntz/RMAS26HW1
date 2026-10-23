# Instructions: how to work on and submit the homework

The homework text is in the PDF for your version in the `zadatak/` folder. This file explains how to set up the tools, work in the repository and submit the homework.

## 1. Install the tools

1. **IntelliJ IDEA**, free version: [jetbrains.com/idea](https://www.jetbrains.com/idea/download/).
2. **Git**, if you don't have it: [git-scm.com](https://git-scm.com/downloads). It is usually already installed on macOS and Linux.
3. **A GitHub account**, if you don't have one: [github.com](https://github.com).

## 2. Turn off AI in IntelliJ

The homework is done **without AI**, and that includes code completion in the editor.

1. Open **Settings** (Windows/Linux: `Ctrl+Alt+S`, macOS: `Cmd+,`).
2. In the search box at the top left, type **inline completion** and turn off all options that appear.
3. In **Settings → Plugins → Installed**, search for **AI** and disable all AI plugins, e.g. *JetBrains AI Assistant*, *GitHub Copilot* and similar.
4. Restart IntelliJ.

Basic completion (the list of suggestions while you type a function name) may stay on. Only completion that suggests whole lines or blocks of code is turned off.

## 3. Get your repository

1. Open the homework link on **Classmoji** and accept the homework. You will get your own repository on GitHub.
2. On the repository page, click the green **Code** button and copy the HTTPS address.
3. In IntelliJ, on the welcome screen, choose **Clone Repository** (or **File → New → Project from Version Control**).
4. Paste the address and click **Clone**. If asked to log in, log in to GitHub.

## 4. First run

1. After opening, IntelliJ loads the project (Gradle) for the first time. This may take a few minutes and needs internet access. Wait until the progress bar at the bottom disappears.
2. Open `src/main/kotlin/Main.kt`.
3. Click the green arrow next to `fun main()` and choose **Run**.
4. `Zdravo, Kotlin!` should be printed at the bottom. If it is, everything is ready.

You write all your code in `src/main/kotlin/`. The data model goes in `Model.kt`, and reading data, queries and output go in `Main.kt`. You may add more files if you want. The `data/` folder with CSV files is used only by version C.

## 5. Commit and push

Commit **as you make progress**, not only at the end. At least 5 commits are required.

1. **Git → Commit** (Windows/Linux: `Ctrl+K`, macOS: `Cmd+K`).
2. Select the files you changed and write a short message about what you did.
3. Click **Commit and Push**, then **Push**.

Examples of good messages:
- `Model: course and course type`
- `Data entry`
- `Average and ECTS`
- `Courses not passed and best grade`
- `Output per semester`

Check on the repository page on GitHub that your commits are visible.

## 6. Submission

- Your submission is your **last push before the deadline**. Commits after the deadline do not count.
- You don't send anything by email. The teaching assistant takes the code directly from your repository.

## Common problems

| Problem | Solution |
|---|---|
| "No JDK" or "Project JDK is not defined" | **File → Project Structure → Project → SDK → Download JDK**, choose version 21. |
| Red lines everywhere after opening | Wait for Gradle to finish loading. If that doesn't help, click the elephant icon (**Load Gradle Changes**) or **File → Reload All from Disk**. |
| Push asks for a password and doesn't accept it | GitHub doesn't accept passwords. In IntelliJ, log in via **Settings → Version Control → GitHub → Add Account → Log In via GitHub**. |
| There is no green arrow | Check that `Main.kt` is in `src/main/kotlin/` and has `fun main()`. |
