---
Title: Git commands
tags: TechSkills
DateStarted: 2022-12-10
DateModified: 2023-12-08
status: 
sr-due: 2023-07-02
sr-interval: 4
sr-ease: 273
---
## Tools

- [前端工程化 | 使用 commitizen 规范你的 commit message！ | 你真是一个美好的人类](https://blog.juanertu.com/archives/5aa66889.html)
- [Writing Better Commits. Writing better commits with the… | by Erxk | Mar, 2023 | ITNEXT](https://itnext.io/writing-better-commits-6a1691c12772)

## Use
### Submodules
- Add/ Clone a submodule: 
	- `git submodule add [url-to-submodule] path-to-submodule`
- Rename/ Move a submodule: 
	- `mv old-submodule-name new-submodule-name`
	- Update git config to reflect the new name:
		- `git config -f .gitmodules --rename-section submodule.old_submodule_name submodule.new_submodule_name`
		- 或者
			- Update `.gitmodules`:  `git mv old_submodule_name new_submodule_name`
			- Update git internal records: `git submodule sync --recursive`
- Remove a submodule: 
	- Remove from `.gitmodules` file:  `git submodule deinit -f path/to/submodule`
	- Remove from the working tree and index: `git rm -f path/to/submodule`
- Commit change to a submodule: 
	- `cd submodule` --> `git add .` --> `git commit -m"..."` ...
	- Update the main repo: `cd ..` --> `git add .` --> ...
### Token
- [Site Unreachable](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens)
- gitee token
	- 098d55a41dcdafae1fcaaac18ec5e000
- ubuntu_git token (1113-0213/ 90 days)
	-  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
- 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
- To reduce the time entering username and password: 
	- [Git - git-credential-cache Documentation](https://git-scm.com/docs/git-credential-cache
	- [github - Git asks for username every time I push - Stack Overflow](https://stackoverflow.com/questions/11403407/git-asks-for-username-every-time-i-push)
### Download
#### Update 
- Update Git in Ubuntu
	- [How to update Git in Ubuntu + Windows Subsystem for Linux – 7.dev](https://7.dev/how-to-update-git-in-ubuntu-windows-subsystem-for-linux/#:~:text=How%20to%20update%20Git%20in%20Ubuntu%20%2B%20Windows,and%20install%20Git%20from%20the%20new%20source%3A%20)
- Update Git on windows
	- `git update-git-for-windows`
	- [How to upgrade Git on Windows to the latest version - Stack Overflow](https://stackoverflow.com/questions/13790592/how-to-upgrade-git-on-windows-to-the-latest-version)
#### 1. Download Git/ WSL for Windows

- [Git for Windows](https://gitforwindows.org/)
- [Install WSL | Microsoft Learn](https://docs.microsoft.com/en-us/windows/wsl/install-win10)

### Config

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
### Work with Remote Repository

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
- ![[z-Assets/Pasted image 20230216170600.png]]

### GIT GUI

gitk (使用这个工具，可以在 GUI 下确认提交记录。)  
PAT Ubuntu 不能执行 **git clone 或 git pull** 操作，退出用 windows cmd 执行，执行前：  
新建文件夹> git init > …  
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  
[  
](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-personal-account-on-github/managing-your-membership-in-organizations/publicizing-or-hiding-organization-membership)
![[git-cheat-sheet-education.pdf]]
