# HOW TO BACKTRACK

Favorite: No
Archived: No
Project: Git & GitHub (https://www.notion.so/Git-GitHub-850ba1cf02844de08bc53419fe94730c?pvs=21)

# **Backtracking Intro**

When working on a Git project, sometimes we make changes that we want to get rid of. Git offers a few eraser-like features that allow us to undo mistakes during project creation. In this lesson, we’ll learn some of these features.

To start out, let’s review the basic Git workflow.

**Instructions**

1. Checkpoint 1**.**
You are in a Git project titled **hamlet-prince-of-denmark**. In the code editor, you’ll be working on **scene-5.txt**. Here, Hamlet encounters the ghost of his father. Add this text to the file:

`Ghost: My hour is almost come,When I to sulphurous and tormenting flamesMust render up myself.`

```
Hamlet: Act 1, Scene 5

Enter Ghost and Hamlet

Hamlet:
Where wilt thou lead me? speak; I'll go no further

Ghost:
Mark me.

Hamlet:
I will
```

2. Checkpoint 2**.**
From the terminal, add **scene-5.txt** to the staging area.

```bash
git add .
```

3. Checkpoint 3**.**
Commit the changes to the repository with a good commit message.

```bash
git commit -m "update"
[master 300012b] update
 1 file changed, 4 insertions(+), 1 deletion(-)
```

---

# **head commit**

In Git, the commit you are currently on is known as the `HEAD` commit. In many cases, the most recently made commit is the `HEAD` commit.

To see the `HEAD` commit, enter:

```bash
git show HEAD
```

The output of this command will display everything the [git log command](https://www.codecademy.com/en/courses/learn-git/lessons/git-workflow/exercises/git-log) displays for the `HEAD` commit, plus all the file changes that were committed.

**Instructions**

1. Checkpoint 1
Enter the command to show the `HEAD` commit.
Notice the output. The ghost’s most recently added line is in green text.

```bash
$ git show HEAD
commit 300012b44c57dbc30c9c65b213785216b1bf7347
Author: codecademy <ccuser@codecademy.com>
Date:   Sun Jun 9 02:40:36 2024 +0000

    update

diff --git a/scene-5.txt b/scene-5.txt
index b12dd97..8b19f00 100644
--- a/scene-5.txt
+++ b/scene-5.txt
@@ -11,4 +11,7 @@ Mark me.
 Hamlet:
 I will.
 
-
+Ghost:
+My hout is almost come,
+When I so sulphurous and tormenting flames
+Must render up myself.
```

---

# **git checkout**

What if you decide to change the ghost’s line in the working directory, but then decide you wanted to discard that change?

You could rewrite the line how it was originally, but what if you forgot the exact wording? The command

```bash
git checkout HEAD filename
```

will restore the file in your working directory to look exactly as it did when you last made a commit.

Here, `filename` again is the actual name of the file. If the file is named **changes.txt**, the command would be

```bash
git checkout HEAD changes.txt
```

**Instructions**

1. Checkpoint 1**.**
Change the ghost’s words in some way. Here’s a fun suggestion:
`Ghost: My hour is almost come,When I to sulphurous and tormenting balloonsMust render up myself.` 

2. Checkpoint 2**.**
From the terminal, use `git diff` to see the difference between **scene-5.txt** as it appears in the working directory vs. how it appears in your last commit.

```bash
$ git diff
diff --git a/scene-5.txt b/scene-5.txt
index 8b19f00..85de587 100644
--- a/scene-5.txt
+++ b/scene-5.txt
@@ -13,5 +13,5 @@ I will.
 
 Ghost:
 My hout is almost come,
-When I so sulphurous and tormenting flames
+When I so sulphurous and tormenting balloons
 Must render up myself.
```

3. Checkpoint 3.
Use the new Git command to restore the file in your working directory to look as it did when you last made a commit.
Close the **scene-5.txt** file and then re-open it to see that the changes you had previously made to the ghost’s line have been discarded.

```bash
$ git checkout HEAD scene-5.txt
```

---

# **more git add**

The **hamlet** repository we are working on contains five files. In Git, it’s common to change many files, add those files to the staging area, and [commit](https://www.codecademy.com/resources/docs/git/commit) them to a repository in a single commit.

For example, say you want to change the character “LARRY” to “LAERTES” in the script. The name currently appears in two files. After you change the name in both files, you could add the changed files to the staging area with:

```bash
git add filename_1 filename_2
```

Note the word `filename` above refers to the name of the file you are adding to the staging area, such as **scene-3.txt**.

Scene-3.txt

```
Hamlet: Act 1, Scene 3

A room in Polonius' house.

Enter LARRY and OPHELIA

LARRY
My necessaries are embark'd: farewell:
And, sister, as the winds give benefit
And convoy is assistant, do not sleep,
But let me hear from you.

OPHELIA
Do you doubt that?

LARRY
For Hamlet and the trifling of his favour,
Hold it a fashion and a toy in blood,
A violet in the youth of primy nature,
Forward, not permanent, sweet, not lasting,
The perfume and suppliance of a minute; No more.

OPHELIA
No more but so?
```

Scene-7.txt

```
Hamlet: Act 4, Scene 7

Another room in the castle.

Enter KING CLAUDIUS and LARRY

KING CLAUDIUS
Now must your conscience my acquaintance seal,
And you must put me in your heart for friend,
Sith you have heard, and with a knowing ear,
That he which hath your noble father slain
Pursued my life.

LARRY
It well appears: but tell me
Why you proceeded not against these feats,
So crimeful and so capital in nature,
As by your safety, wisdom, all things else,
You mainly were stirr'd up.

KING CLAUDIUS
O, for two special reasons;
Which may to you, perhaps, seem much unsinew'd,
But yet to me they are strong. The queen his mother
Lives almost by his looks; and for myself--
My virtue or my plague, be it either which--
She's so conjunctive to my life and soul,
That, as the star moves not but in his sphere,
I could not but by her. The other motive,
Why to a public count I might not go,
Is the great love the general gender bear him;
Who, dipping all his faults in their affection,
Would, like the spring that turneth wood to stone,
Convert his gyves to graces; so that my arrows,
Too slightly timber'd for so loud a wind,
Would have reverted to my bow again,
And not where I had aim'd them.

LARRY
And so have I a noble father lost;
A sister driven into desperate terms,
Whose worth, if praises may go back again,
Stood challenger on mount of all the age
For her perfections: but my revenge will come.
```

**Instructions**

1. Checkpoint 1**.**
The code editor is open to **scene-3.txt** and **scene-7.txt**. In **scene-3.txt**, everywhere you see the name “LARRY” change it to “LAERTES.”

2. Checkpoint 2**.**
Now change all instances of “LARRY” to “LAERTES” in **scene-7.txt**.

3. Checkpoint 3 Step instruction is unavailable until previous steps are completed**3.**
Add the files to the staging area together using a single git command.

```bash
$ git add scene-3.txt scene-7.txt
```

---

# **git reset I**

Great! The files you’ve added to the staging area belong in the same commit.

What if, before you commit, you accidentally delete an important line from **scene-2.txt**? Unthinkingly, you add **scene-2.txt** to the staging area. The file change is unrelated to the Larry/Laertes swap and you don’t want to include it in the commit.

Scene-2.txt

```
Hamlet: Act 1, Scene 2

A room of state in the castle.

Enter KING CLAUDIUS, QUEEN GERTRUDE, HAMLET, POLONIUS, LAERTES, VOLTIMAND,
CORNELIUS, Lords, and Attendants

KING CLAUDIUS
Though yet of Hamlet our dear brother's death
The memory be green, and that it us befitted
To bear our hearts in grief and our whole kingdom
To be contracted in one brow of woe,
Yet so far hath discretion fought with nature
That we with wisest sorrow think on him,
Together with remembrance of ourselves.
Therefore our sometime sister, now our queen,
The imperial jointress to this warlike state,
Have we, as 'twere with a defeated joy,--
With an auspicious and a dropping eye,
With mirth in funeral and with dirge in marriage,
In equal scale weighing delight and dole,--
Taken to wife: nor have we herein barr'd
Your better wisdoms, which have freely gone
With this affair along. For all, our thanks.
Now follows, that you know, young Fortinbras,
Holding a weak supposal of our worth,
Or thinking by our late dear brother's death
Our state to be disjoint and out of frame,
Colleagued with the dream of his advantage,
He hath not fail'd to pester us with message,
Importing the surrender of those lands
Lost by his father, with all bonds of law,
To our most valiant brother. So much for him.
Now for ourself and for this time of meeting:
Thus much the business is: we have here writ
To Norway, uncle of young Fortinbras,--
Who, impotent and bed-rid, scarcely hears
Of this his nephew's purpose,--to suppress
His further gait herein; in that the levies,
The lists and full proportions, are all made
Out of his subject: and we here dispatch
You, good Cornelius, and you, Voltimand,
For bearers of this greeting to old Norway;
Giving to you no further personal power
To business with the king, more than the scope
Of these delated articles allow.
```

We can *unstage* that file from the staging area using

```bash
git reset HEAD filename
```

This command *resets* the file in the staging area to be the same as the `HEAD` commit. It does not discard file changes from the working directory, it just removes them from the staging area.

**Instructions**

1. Checkpoint 1**.**
To try out the new command, let’s make a mistake on purpose!

2. Checkpoint 2**.**
From the terminal, add **scene-2.txt** to the Git staging area.

3. Checkpoint 3**.**
Now check the `status` of the Git project.
In the output, notice **scene-2.txt** under “Changes to be committed”.

```bash
$ git add .
$ git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        modified:   scene-2.txt
        modified:   scene-3.txt
        modified:   scene-7.txt

```

4. Checkpoint 4**.**
Use the new Git command to *unstage* **scene-2.txt** from the staging area.
Notice in the output, “Unstaged changes after reset”:
`M   scene-2.txt`
    ◦ `M` is short for “modification”

```bash
$ git reset HEAD scene-2.txt
Unstaged changes after reset:
M       scene-2.txt
```

5. Checkpoint 5**.**
Now that changes made to **scene-2.txt** have been booted out of the staging area, you’re ready to commit. From the terminal, make a commit to save the Larry/Laertes name swap in **hamlet**.

---

# **git reset II**

Creating a project is like hiking in a forest. Sometimes you take a wrong turn and find yourself lost.

Just like retracing your steps on that hike, Git enables you to rewind to the part before you made the wrong turn. You can do this with:

```bash
git reset commit_SHA
```

This command works by using the first 7 characters of the SHA of a previous [commit](https://www.codecademy.com/resources/docs/git/commit). For example, if the SHA of the previous commit is `5d692065cf51a2f50ea8e7b19b5a7ae512f633ba`, use:

```bash
git reset 5d69206
```

`HEAD` is now set to that previous commit.

**Instructions**

1. Checkpoint 1**.**
From the terminal, print out your Git commit log.
**Note**: If your cursor gets stuck in “git log” mode in the terminal, press q on your keyboard to escape.

```bash
$ git log
commit a107cb6b3087b5a3aae89029de18d9309cf9f9c7
Author: codecademy <ccuser@codecademy.com>
Date:   Sun Jun 9 02:58:10 2024 +0000

    update

commit d640dc3b22b3ee1d0a6e87477a35fd5e75c0712e
Author: codecademy <ccuser@codecademy.com>
Date:   Thu Nov 5 13:19:17 2015 -0500

    Complete ghost line of dialogue

commit 7be7ec672af73cf31ef72c92e3374fd4e29c675a
Author: danasselin <johndoe@example.com>
Date:   Tue Nov 3 17:15:05 2015 -0500

    Add first page of scene-7.txt

commit 83f7b3591f4ab7aedb3160388b59e65ee1cd94a2
Author: danasselin <johndoe@example.com>
Date:   Tue Nov 3 17:14:48 2015 -0500

    Add first page to scene-5.txt

commit 5d692065cf51a2f50ea8e7b19b5a7ae512f6
```

2. Checkpoint 2**.**
From the terminal, enter the command to `reset` to a previous commit, using the first 7 characters of one of the past commit SHAs in your Git log.
Next, print the Git commit log again.
Notice anything interesting? The commits that came after the one you reset to are gone. The `HEAD` commit has been reassigned. You just changed history.

```bash
$ git reset d640dc3
Unstaged changes after reset:
M       scene-2.txt
M       scene-3.txt
M       scene-7.txt
```

---

# **git reset review**

To better understand `git reset commit_SHA`, notice the diagram on the right. Each circle represents a commit.

**Before reset**:

- `HEAD` is at the *most recent commit*

**After resetting**:

- `HEAD` goes to a *previously made commit* of your choice
- The gray commits are no longer part of your project
- You have in essence rewound the project’s history

![Untitled](HOW%20TO%20BACKTRACK%201a15e9adbb164290a61037456c39ba78/Untitled.png)

---

# **Generalizations**

Congratulations! You’ve learned three different ways to backtrack in Git. You can use these skills to undo changes made to your Git project.

Let’s take a moment to review the new commands:

- `git checkout HEAD filename`: Discards changes in the working directory.
- `git reset HEAD filename`: Unstages file changes in the staging area.
- `git reset commit_SHA`: Resets to a previous commit in your commit history.

Additionally, you learned a way to add multiple files to the staging area with a single command:

```bash
git add filename_1 filename_2
```

---

**Staging Multiple Files**

```bash
$ git add scene-5.txt scene-7.txt
$ git status
On branch master
Changes to be committed:
  (use ""git reset HEAD <file>..."" to unstage)

        modified:   scene-5.txt
        modified:   scene-7.txt
```

In Git, the **`git add filename_1 filename_2`** command is used to add multiple files to the staging area at once.

You can use **`git status`** to check if you properly added your files to the staging area.

**Showing Latest Commit Log**

```bash
$ git show HEAD
commit 735359632f3ca3fe572484a4ec3e0d7b0d9c8f2d
Author: codecademy <exampleuser@codecademy.com>
Date:   Wed Jul 6 10:20:58 2016 -0400

    scene-5.txt

diff --git a/scene-5.txt b/scene-5.txt
index b12dd97..5dd5d4e 100644
--- a/scene-5.txt
+++ b/scene-5.txt
@@ -12,3 +12,7 @@ Hamlet:
I will.

+Ghost:
+My hour is almost come,
+When I to sulphurous and tormenting flames
+Must render up myself.
\ No newline at end of file
```

In Git, the commit you are currently on is known as the **`HEAD`** commit.

The output of the **`git show HEAD`** command will display everything the **`git log`** command displays for the **`HEAD`** commit, plus all the file changes that were committed.

**Rolling Back to Last Commit**

```bash
$ git checkout HEAD scene-5.txt
$ git diff
$
```

In Git, the **`git checkout HEAD filename`** command rolls back all changes that have been made to **`filename`** since the last commit. In other words, this command will change your working directory to look exactly as it did when you last made a commit.

You can use the **`git diff`** command to see if the rollback was successful. If **`git diff`** doesn’t output anything, this means your working directory matches your last commit.

**Remove File from Staging**

```bash
$ git reset HEAD scene-3.txt
Unstaged changes after reset:
M       scene-3.txt
```

In Git, the **`git reset HEAD filename`** command will remove **`filename`** from the staging area. Note that this command does *not* discard file changes from the working directory. You might use this command if you’ve added a file to the staging area, but the file includes incorrect edits.

You can use the **`git status`** command to make sure your file was properly removed from the staging area.

**Git Reset Using SHA**

```bash
$ git log
commit 9d63f80111447544c303e9f1776fa08593a87310
Author: codecademy <exampleuser@codecademy.com>
Date:   Wed Jan 13 18:55:53 2021 +0000

    Added updates to the file

commit 3ba6efbeece6ed530d85de5e313e52123fdf8cb4
Author: codecademy <exampleuser@codecademy.com>
Date:   Wed Jan 6 10:11:13 2021 -0400

    Completed first line of dialogue

$ git reset 3ba6efb
```

In Git, the **`git reset commit_SHA`** command can be used to set **`HEAD`** to the **`commit_SHA`** commit. The **`commit_SHA`** argument is the first seven digits of a previous commit’s [SHA](https://en.wikipedia.org/wiki/Secure_Hash_Algorithms). In this example, the **`HEAD`** was reset to the commit made on **`Wed Jan 6`**.

You can use **`git log`** to see a record of previous commits and their SHA values.