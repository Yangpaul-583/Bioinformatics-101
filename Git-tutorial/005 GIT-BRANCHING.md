# GIT BRANCHING

Favorite: No
Archived: No
Project: Git & GitHub (https://www.notion.so/Git-GitHub-850ba1cf02844de08bc53419fe94730c?pvs=21)

# **git branch**

Up to this point, you’ve practiced in a single Git [branch](https://www.codecademy.com/resources/docs/git/branch). (Note: GitHub has changed the naming convention of the main branch from `master` to `main`.We will be updating the instructions and code workspaces soon to reflect that. In the meantime, `master` refers to `main`).

Git allows us to create *branches* to experiment with versions of a project. Imagine you want to create a version of a story with a happy ending. You can create a new branch and make the happy ending changes to that branch only. It will have no effect on the `master` branch until you’re ready to [merge](https://www.codecademy.com/resources/docs/git/merge) the happy ending to the master branch.

In this lesson, we’ll be using Git branching to develop multiple versions of a resumé.

You can use the command below to answer the question: “which branch am I on?”

```bash
git branch
```

# **branching overview**

![Untitled](GIT%20BRANCHING%20430b0f5cc3554bb2a46a70150b70afc6/Untitled.png)

The diagram to the right illustrates branching.

- The circles are commits, and together form the Git project’s [commit](https://www.codecademy.com/resources/docs/git/commit) history.
- *New Branch* is a different *version* of the Git project. It contains commits from the main [branch](https://www.codecademy.com/resources/docs/git/branch) but also has commits that it does not have.

# **git branch 2**

Right now, the Git project has only one branch: `master`.

To create a new [branch](https://www.codecademy.com/resources/docs/git/branch), use:

```bash
git branch new_branch
```

Here `new_branch` would be the name of the new branch you create, like `photos` or `blurb`. Be sure to name your branch something that describes the purpose of the branch. Also, branch names can’t contain whitespaces: `new-branch` and `new_branch` are valid branch names, but `new branch` is not.

Let’s create a new version of a resumé to apply for a fencing instructor role.

Create a new branch called `fencing`.

Remember to spell the word “fencing” correctly.

Next, view your branches as you did in the previous exercise.

Notice in the output there now appear two branches: `master` and `fencing`.

```bash
$ git branch fencing
$ git branch
  fencing
* master
```

# **git checkout**

Great! You just created a new [branch](https://www.codecademy.com/resources/docs/git/branch).

The `master` and `fencing` branches are identical: they share the same exact [commit](https://www.codecademy.com/resources/docs/git/commit) history. You can switch to the new branch with

```bash
git checkout branch_name
```

Here, `branch_name` is the name of the branch. If the branch’s name is `skill`

```bash
git checkout skill
```

Once you switch branches, you will now be able to make commits on the branch that have no impact on `master`.

You can continue your workflow, while `master` stays intact!

**Instructions**

1. Checkpoint 1 Passed**1.**
Switch to the `fencing` branch from the `master` branch.
2. Checkpoint 2 Passed**2.**
Use `git branch` to verify that you have switched branches.
In the output, notice the `*` is now over the `fencing` branch.

```bash
$ git checkout fencing
Switched to branch 'fencing'
$ git branch
* fencing
  master
```

# **commit on a new branch**

Congratulations! You have switched to a new [branch](https://www.codecademy.com/resources/docs/git/branch). All the commands you do on `master`, you can also do on this branch.

![Untitled](GIT%20BRANCHING%20430b0f5cc3554bb2a46a70150b70afc6/Untitled%201.png)

For example, to add files to the staging area, use:

```bash
git add filename
```

And to [commit](https://www.codecademy.com/resources/docs/git/commit), use:

```bash
git commit -m "Commit message"
```

In a moment, you will make a commit on the `fencing` branch. On the far right, the diagram shows what will happen to the Git project.

# **git merge**

What if you wanted to include all the changes made to the `fencing` [branch](https://www.codecademy.com/resources/docs/git/branch) on the `master` branch? We can easily accomplish this by *merging* the branch into master with:

```bash
git merge branch_name
```

For example, if I wanted to [merge](https://www.codecademy.com/resources/docs/git/merge) the `skills` branch to master, I would enter

```bash
git merge skills
```

In a moment, you’ll merge branches. Keep in mind:

- Your goal is to update `master` with changes you made to `fencing`.
- `fencing` is the giver branch, since it provides the changes.
- `master` is the receiver branch, since it accepts those changes.

```bash
$ git checkout master
Switched to branch 'master'
$ git merge fencing
Updating 79a1cc5..7cd4510
Fast-forward
 resume.txt | 2 +-
 1 file changed, 1 insertion(+), 1 deletion(-)
```

# **merge conflict I**

The [merge](https://www.codecademy.com/resources/docs/git/merge) was successful because `master` had not changed since we made a [commit](https://www.codecademy.com/resources/docs/git/commit) on `fencing`. Git knew to simply update `master` with changes on `fencing`.

What would happen if you made a commit on `master` *before* you merged the two branches? Furthermore, what if the commit you made on `master` altered the same exact text you worked on in `fencing`? When you switch back to `master` and ask Git to merge the two branches, Git doesn’t know which changes you want to keep. This is called a *merge conflict*.

```bash
$ git add .
$ git commit -m "new commit"
[master 8b83546] new commit
 2 files changed, 1 insertion(+), 1 deletion(-)
 create mode 100644 .DS_Store
$ git checkout fencing
Switched to branch 'fencing'
$ git add .
$ git commit -m "new changes on fencing"
[fencing 8e90930] new changes on fencing
 1 file changed, 1 insertion(+), 1 deletion(-)
```

# **merge conflict II**

Let’s say you decide you’d like to [merge](https://www.codecademy.com/resources/docs/git/merge) the changes from `fencing` into `master`.

Here’s where the trouble begins!

You’ve made commits on separate branches that alter the same line in conflicting ways. Now, when you try to merge `fencing` into `master`, Git will not know which version of the file to keep.

```bash
$ git checkout master
Switched to branch 'master'
$ git merge fencing
Auto-merging resume.txt
CONFLICT (content): Merge conflict in resume.txt
Automatic merge failed; fix conflicts and then commit the result.
```

In the code editor, look at **resume.txt**. Git uses markings to indicate the `HEAD` (master) version of the file and the `fencing` version of the file, like this:

```bash
<<<<<<< HEAD
master version of line
=======
fencing version of line
>>>>>>> fencing
```

**Note**: If the markings are not showing in `resume.txt`, please close `resume.txt` and re-open via the folder icon at the top left corner of the editor.

Git asks us which version of the file to keep: the version on `master` or the version on `fencing`. You decide you want the `fencing` version.

From the code editor:

Delete the content of the line as it appears in the `master` branch

Delete **all of Git’s special markings** including the words `HEAD` and `fencing`. If any of Git’s markings remain, for example, `>>>>>>>` and `=======`, the conflict remains.

```bash
$ git merge fencing
Auto-merging resume.txt
CONFLICT (content): Merge conflict in resume.txt
Automatic merge failed; fix conflicts and then commit the result.
$ git add resume.txt
$ git commit -m "Resolve merge conflict"
[master a9befa6]  Resolve merge conflict
```

# **delete branch**

In Git, branches are usually a means to an end. You create them to work on a new project feature, but the end goal is to [merge](https://www.codecademy.com/resources/docs/git/merge) that feature into the `master` [branch](https://www.codecademy.com/resources/docs/git/branch). After the branch has been integrated into `master`, it has served its purpose and can be deleted.

The command

```bash
git branch -d branch_name
```

will delete the specified branch from your Git project.

Now that `master` contains all the file changes that were in `fencing`, let’s delete `fencing`.

# **Generalizations**

Let’s take a moment to review the main concepts and commands from the lesson before moving on.

- Git *branching* allows users to experiment with different versions of a project by checking out separate *branches* to work on.

The following commands are useful in the Git [branch](https://www.codecademy.com/resources/docs/git/branch) workflow.

- `git branch`: Lists all a Git project’s branches.
- `git branch branch_name`: Creates a new branch.
- `git checkout branch_name`: Used to switch from one branch to another.
- `git merge branch_name`: Used to join file changes from one branch to another.
- `git branch -d branch_name`: Deletes the branch specified.