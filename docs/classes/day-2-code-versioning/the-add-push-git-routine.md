# Git Routine 2:  Extend your current code and use Git, GitHub to Keep track of Changes and collaborate

In this exercise, we will use the personal forks as the repository where each of us will contribute.

To do that we are going to make a clone of your version of the repository.

Use the command line tool `mkdir` to make a directory with your user name.

My user name is _adeslatt_

```bash
mkdir adeslatt
```

Move into that directory using the command line tool `cd` to `change directory` into your user name

```bash
cd adeslatt
```

In this case now I am in an empty directory.

Now I am going to clone my forked version of the NIH-NICHD exampleVolcanoPlot repository.

```bash
git clone https://github.com/Wellstein-lab/exampleVolcanoPlotNotebook.git
```

Now we need to move into the exampleVolcanoPlotNotebook directory.

```bash
cd exampleVolcanoPlotNotebook
```

Type as the following command to see where the upstream location of our file is.

## A very handy command I use daily *`git status`*

The *`git status`* command helps us inspect to see if there are any changes to our local copy of our repository.

```bash
git status
```

You should see something like:

```bash
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
```
## Edit a file

We can edit a file inside your folder *`README.md`*

Let's use nano or the notebook interface to edit tje README.md file.

First lets navigate to the directory for this class.

```bash
cd <my username>/exampleVolcanoPlotNotebook
```

Next lets edit a file README.md

You can use Nano or you can double click the file on the left and add some lines to the readme.


```
Learn about Zenodo here: https://zenodo.org

```

When ready to save the file by using these shortcut keys. in Nano or just hit x and it will ask you to save.

<kbd> **`CTRL`**  </kbd> `+`  <kbd> **`O`** </kbd>

This will declare your willingness to save the file. Click <kbd> **`ENTER`**  </kbd> to verify that you want to save the file.


Now Close the file and exit from nano with the the shortcut:
<kbd> **`CTRL`**  </kbd> `+`  <kbd> **`X`** </kbd>

Awesome, your file has just been saved! You can inspect using the `head` command, eg `head README.md`

## Inspect the changes with *`git status`*

```bash
git status
```

which returns something like

```
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md

nothing added to commit but untracked files present (use "git add" to track)
```

We now need to add the modified file to the branch

```bash
git add README.md
```

We also need to write a message denoting what change was done and finalize the addition.

```bash
git commit -m "added useful commands to the README.md"
```

Now we need to execute the last step -- which is to *`push`* the changes to GitHub

```bash
git push
```

Now we can see what we have done with *`git status`*

```bash
git status
```

And we see we are now up to date.

## Contributing to the main branch

Now we have the changes in our repository.   We are out of sync potentially with the main repository.  Lets inspect.

In the chrome browser, navigate to your repository on GitHub and inspect our local changes.

<img src="/../../img/GitHubContributingInspectingTheBranchAfterMakingLocalChanges.png" width=650>

First, we synchronize with the main branch, by pressing the *`sync`* button.

<img src="/../../img/GitHubContributingAfterSynchronizingWithMain.png" width=650>

Next, we make a pull request, this allows us to offer our changes to the main repository.
<img src="/../../img/GitHubContributingMakingAPullRequest.png" width=650>

As the repository owner, I can inspect and accept or not accept all the proposed changes.

<img src="/../../img/GitHubContributingInspectingPullRequestsInMain.png" width=650>

## Conclusion of todays class

Recap

_ You learned about *`Git`* and *`GitHub`*
_ You *`Fork`*ed a repository
_ You synchronized your *`Fork`* to the main repository 
- You made a contribution with a *`Pull Request`*

You have entered the world of documenting your work using GitHub -- Congratulations!!

## [Return to Agenda](day-2-code-versioning.md) 





