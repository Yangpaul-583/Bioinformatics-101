# Project: SnapFit Robots, Inc.

Favorite: No
Archived: No
Project: Git & GitHub (https://www.notion.so/Git-GitHub-850ba1cf02844de08bc53419fe94730c?pvs=21)

Now that you’ve had more practice with the Git workflow, let’s solidify your new skills even more.

In this project, you will be working on assembly instructions for Snap-Fit Robots Inc., a build-it-yourself robot company.

```
SNAPFIT ROBOTS PRODUCT DISCLAIMER

Your Snapfit Robot Model i075 is provided with guarantee of limited 1-year warranty only. Outside of maintenance and malfunction descriptions covered in the warranty, customer shall make no claims of any kind, either express or implied, including but not limited to warranties of sellability, fitness for specific usage, of title, or of noninfringement of third and fourth party rights, and/or rights to attend robot parties. Use of the product by uninformed user is at the user’s risk.

```

**1.**Initialize a new Git project.

**2.**Check the status of the Git project.
You will see multiple files listed in the output as “Untracked”.

**3.**Add each file to the Git staging area.

**4.**Check the status of the Git project again.

**5.**Make a commit.

**6.**View your Git commit log.
If your cursor is stuck in Git log mode, press “q” on your keyboard to escape.

**7.**Include this line in **disclaimer.txt**:

```
Warning: For best battery life, do not leave robot battery charging overnight.

```

**8.**Add the file to the staging area.

**9.**Now make a commit.

**10.**View your Git commit log again to identify your commit.

**11.**Revise each file in whatever ways you’d like. Then add your changes to the staging area and make another commit.

```bash
$ git init
Initialized empty Git repository in /home/ccuser/workspace/snapfit-robots/.git/
$ git status
On branch master

Initial commit

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        disclaimer.txt
        instructions.txt
        warranty.txt

nothing added to commit but untracked files present (use "git add" to track)
```

```bash
$ git add .
$ git status
On branch master

Initial commit

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

        new file:   disclaimer.txt
        new file:   instructions.txt
        new file:   warranty.txt
$ git commit -m "added new files"
[master (root-commit) f88dfb7] added new files
 3 files changed, 70 insertions(+)
 create mode 100644 disclaimer.txt
 create mode 100644 instructions.txt
 create mode 100644 warranty.txt

$ git log
commit f88dfb7f942907fa4f9263f2c81d8ae78a418bc3
Author: codecademy <ccuser@codecademy.com>
Date:   Sat Jun 8 07:50:34 2024 +0000

    added new files
```

```bash
$ git add .
$ git commit -m "update"
[master 9534d5d] update
 1 file changed, 1 insertion(+)
$ git log
commit 9534d5d558b8a31667c01aa66e981ff5118e7b03
Author: codecademy <ccuser@codecademy.com>
Date:   Sat Jun 8 07:51:43 2024 +0000

    update

commit f88dfb7f942907fa4f9263f2c81d8ae78a418bc3
Author: codecademy <ccuser@codecademy.com>
Date:   Sat Jun 8 07:50:34 2024 +0000

    added new files
```