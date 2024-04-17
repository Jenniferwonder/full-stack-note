---
title: Git commands
tags:
  - TechSkills
DateStarted: 2022-12-10
DateModified: 2024-04-17
status: 
---

## Tools

- [前端工程化 | 使用 commitizen 规范你的 commit message！ | 你真是一个美好的人类](https://blog.juanertu.com/archives/5aa66889.html)
- [Writing Better Commits. Writing better commits with the… | by Erxk | Mar, 2023 | ITNEXT](https://itnext.io/writing-better-commits-6a1691c12772)

## Use

### Git Autocomplete for Windows

> Install Clink

- ⭐[Overview | Clink](https://chrisant996.github.io/clink/)
- [GitHub - cmderdev/cmder: Lovely console emulator package for Windows](https://github.com/cmderdev/cmder)
- [GitHub - vladimir-kotikov/clink-completions: Completion files to clink util](https://github.com/vladimir-kotikov/clink-completions?tab=readme-ov-file#installation)
- [Can I setup auto-complete for git on Windows via cmd.exe? - Stack Overflow](https://stackoverflow.com/questions/6464610/can-i-setup-auto-complete-for-git-on-windows-via-cmd-exe/75762472#75762472)

### Auto Correct

- `git config --global help.autocorrect 1`
  - 命令中的 `1` 指接受默认纠错等待时间为 `0.1 s`
  - ![[z-Git Commands.png|500]]
  - Reference: [How to Set Up Auto-Complete for Git Commands on Windows cmd.exe | by Yann Mulonda | Medium](https://yannmjl.medium.com/how-to-set-up-auto-complete-for-git-commands-on-windows-cmd-exe-687424d2f142)

### Submodules

- Add/ Clone a submodule:
  - `git submodule add [url-to-submodule] path-to-submodule`
- Rename/ Move a submodule:
  - `mv old-submodule-name new-submodule-name`
  - Update git config to reflect the new name:
    - `git config -f .gitmodules --rename-section submodule.old_submodule_name submodule.new_submodule_name`
    - 或者
      - Update `.gitmodules`: `git mv old_submodule_name new_submodule_name`
      - Update git internal records: `git submodule sync --recursive`
- Remove a submodule:
  - Remove from `.gitmodules` file: `git submodule deinit -f path/to/submodule`
  - Remove from the working tree and index: `git rm -f path/to/submodule`
- Commit change to a submodule:
  - `cd submodule` --> `git add .` --> `git commit -m"..."` ...
  - Update the main repo: `cd ..` --> `git add .` --> ...

### [[Git Token]]

### [[GitHub Pages Deployment]]

### Download

#### Update

- Update Git in Ubuntu
  - [How to update Git in Ubuntu + Windows Subsystem for Linux – 7.dev](https://7.dev/how-to-update-git-in-ubuntu-windows-subsystem-for-linux/#:~:text=How-to-update-Git-in-Ubuntu-%2B-Windows,and-install-Git-from-the-new-source%3A-)
- Update Git on windows
  - `git update-git-for-windows`
  - [How to upgrade Git on Windows to the latest version - Stack Overflow](https://stackoverflow.com/questions/13790592/how-to-upgrade-git-on-windows-to-the-latest-version)

#### 1. Download Git/ WSL for Windows

- [Git for Windows](https://gitforwindows.org/)
- [Install WSL | Microsoft Learn](https://docs.microsoft.com/en-us/windows/wsl/install-win10)

### Config

#### Commit Case-sensitive file or folder

- `git config core.ignorecase false` to revoke default case-insensitive setting
- `git config get core.ignorecase` to check the setting is true or false

#### 1. Install> git initial configuration

- `git config --global user.name "Jennifer"`
- `git config --global user.email "amazing_coder[@163.com" ](/163.com ) ` (MM: wht_Mobile 6 digit)

#### 2. .gitignore

- Create a `.gitignore`file in the project root folder
- Add folderName of the folder to be ignored in `.gitignore`file

### Version Control in Development

#### 1. Create a local git repository

- In the local repo > `git init`

#### 2. Create a new branch

- `git checkout -b "new branch name"`
- `git branch <new branch name>`

#### 3. Get the existing branch name

- `git branch`

#### 4. Get the git status

- `git status`
- `git log` (to know the commit **hash and message** of different commit)

#### 5. Switch to a new branch

- `git checkout <new branch name>`

#### 6. Add, Commit and Push change to remote repository

- `git commit -am "<message>"`
- `git add <filename>`/ `git add . `/`git add -A` (to add all files)
- `git commit -m"<message>" `
- `git push`

#### 7. Untrack file

- `git rm -r --cached <filename>`

#### 8. Merge change of new branch to the current branch

- `git merge <new branch name>`

#### 9. Resolve a merge conflict

- open the file where the conflict exist
- modify the file to resolve the conflict
- commit the change

#### 10. Restore the previous committed version

- `git reset --hard <commit hash>`
- `git log` (to get the commit hash)
  - Get back to the terminal: `q`
- `git reset --hard origin/master` (the version currently on Github)
- `git reset --hard HEAD` (restore to the previous commit)
- Revert previous commit
  - `git revert <commit hash>`

#### Restore a reset

If you have reset your Git repository to a previous state using `git reset`, and you want to restore it to the state before the reset

- find the commit you want to reset to
  - `git reflog`
  - to recover lost commit due to reset
    - `git fsck --lost-found`
    - 🟨 to restore lost commit
      - `git cherry-pick`
- **soft reset**: changes are still staged. Move your branch pointer back to that commit.
  - `git reset --soft <commit>`
- **mixed reset**: changes are still present but unstaged
  - `git reset --mixed <commit>`
- **hard reset**: will discard any changes you've made since the reset
  - `git reset --hard <commit>`

#### Log commit history hash

`git log`

```bash
git log --oneline        # Compact output with abbreviated commit hashes
git log -n 5             # Show only the last 5 commits
```

#### View changes introduced by a commit

- `git diff <commit_hash>^ <commit_hash>`

#### View files committed in a commit

- shows only the filenames
  `git show --name-only <commit_hash>`
- additionally shows the status of each file (added, modified, deleted)
  `git show --name-status <commit_hash>`

#### View git commit detailed information

- `git show <commit_hash>`

### Work with Remote Repository

#### Rename a branch

![[z-rename-git-branch.png|275]]

> [version control - How can I rename a local Git branch? - Stack Overflow](https://stackoverflow.com/questions/6591213/how-can-i-rename-a-local-git-branch)

#### 1. Connect local repository to remote Github repository

- Create a new repository on Github:
- `git remote add origin https://github.com/Jenniferwonder/Forkify-Project.git`

#### 2. <mark style="background: #FFF3A3A6;">PULL before PUSH</mark>!!!

- `git pull <remote> <branch>`
- ? If your local branch is not tracking a remote branch, you might need to use `git pull <remote> <branch>` to specify the remote and branch explicitly.

#### 3. Push the master branch to the remote repository :

- `git branch -M main `
- `git push -u origin main`
- `git push origin main`(❗Only works in windows cmd)
- `git push -f origin main ` (With the -f tag you will override the remote branch code with your local repo code.)

#### 4. Check remote origin

- `git remote`

#### 5. Remove remote origin

- `git remote rm <remoteName>`

#### 6. Move one repository to another

Reference:

- cd repo2
- git checkout master
- git remote add r1remote **url-of-repo1**
- git fetch r1remote
- git merge r1remote/master --allow-unrelated-histories (将远程旧仓库与本地新仓库合并)
- git remote rm r1remote

### Contribute to Open Source

#### 1. Fork an interested project to your own Github repository

- Github: fork

#### 2. Clone the forked remote repository to local computer

- `git clone https://github.com/your-username/project.git`

#### 3. Create a branch

- `git checkout -b my-feature`
- Switch to an existing branch
  - `git checkout branch-name`
- Check the info about local branches and their tracking status
  - `git branch -vv`

#### 4. Make, Commit and Push changes to the branch of your forked repo

- `git push origin my-feature`

#### 4. Keep fork in sync before UPDATE change to the remote repository

- Before you make any changes, [keep your fork in sync](https://www.freecodecamp.org/news/how-to-sync-your-fork-with-the-original-git-repository/) to avoid merge conflicts:
- `git remote add upstream https://github.com/zero-to-mastery/start-here-guidelines.git `
- `git pull upstream master`
- `git fetch upstream` > `git merge upstream/main`
- ? The `git pull` command is essentially a combination of two other commands: `git fetch` and `git merge`. It fetches the changes from the specified remote and branch and then merges them into your current local branch.

#### 4. Update change from remote to local repository

- `git pull <repository http>`

#### 5. List all your remote

- `git remote -v`

#### 6. Pull Error -unrelated history

- `git pull origin branchname --allow-unrelated-histories`
- ![](https://cdn.jsdelivr.net/gh/jenniferwonder/bimg/full-stack/Pasted-image-20230216170600.png)

### GIT GUI

gitk (使用这个工具，可以在 GUI 下确认提交记录。)  
PAT Ubuntu 不能执行 **git clone 或 git pull** 操作，退出用 windows cmd 执行，执行前：  
新建文件夹> git init > …  
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  
[  
](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-personal-account-on-github/managing-your-membership-in-organizations/publicizing-or-hiding-organization-membership)
![](https://cdn.jsdelivr.net/gh/jenniferwonder/bimg/full-stack/git-cheat-sheet-education.pdf)
