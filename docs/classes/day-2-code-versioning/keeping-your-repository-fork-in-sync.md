## Keeping your Repository Fork in Sync

Let's now fork the repository which held the volcano plot yesterday.  [Fork the https://github.com/NIH-NICHD/exampleVolcanoPlotNotebook](https://github.com/NIH-NICHD/exampleVolcanoPlotNotebook) repository now.

### Let's fork the volcano plot repository

_**Step 1**_ Navigate in your browser window to _https://github.com/NIH-NICHD/exampleVolcanoPlotNotebook

<img src="/../../GitHubNIHNICHDexampleVolcanoPlot.png" width=650>

_**Step 2**_ Create a Fork

In the browser on the right of the screen you see,  _Edit Pins_ _Watch_ and then _Fork_ select _Fork_
Select where you want to fork the repository, your own GitHub repository.

<img src="/../../GitHubNIHNICHDexampleVolcanoPlotCreateAFork.png" width=650>

You will see the progress window that shows the _Forking_ is in progress

<img src="/../../GitHubNIHNICHDexampleVolcanoPlotForkProgress.png" width=650>

Upon success, you will see the following screen

<img src="/../../GitHubNIHNICHDexampleVolcanoPlotForkComplete.png"

## Clone your repository exampleVolcanoPlot.png"

These words _Clone_ _Fork_ _Pull_ are the language of Git and GitHub.   But they mean as follows:

_**Clone**_ - make a working copy of someone elses repository.

_**Fork**_ - make a copy of someone else's repository, but this one I will make edits to and try to make a contribution.

_**Pull**_ - pull a version of the repository

_**Push**_ - push my changes back to the repository.

Yesterday, we cloned a fork of my repository containing the exampleVolcanoPlot.

## Clean up our window so we can work.


### Synchronizing Your Fork

Navigate to your repository within a new *`Chrome browser tab`* on GitHub - https://github/[*`insert your GitHub user name here`*]/exampleVolcanoPlotNotebook.

<img src="/../../img/GitHubKeepingForkInSyncWithMainRepository.png">

In my case, you will see the NIH-NICHD repository commits behind the _adeslatt/exampleVolcanoPlotNotebook_

So I navigate to the button below code and press the <img src="/../../img/GitHubBranchSyncForkButton.png" width=100>

I then get presented the screen:

<img src="/../../img/GitHubUpdatingBranchWithMainRepository.png">

And I press the  <img src="/../../img/GitHubBranchUpdateBranchButton.png" width=100>.

And we have synchronize success.

<img src="/../../img/GitHubBranchUpdateSuccess.png">

## Cloning your Fork of the repository and executing Git 

Today, slightly different, lets use our command function `mkdir` to make a directory with your name on it.

Navigate in the JupyterLab Launcher window to Terminal.

We want to keep in mind that we are workking with a fork of the main repository.

Open the terminal and type.

```bash
mkdir <YOUR GITHUB ID>
```

Change directory into that directory

```bash
cd <YOUR GITHUB ID>
```

Now Clone the repository

```bash
git clone https://github.com/<YOUR GITHUB USERNAME HERE>/exampleVolcanoPlotNotebook.git
```

## All of these steps can also occur from the command line.

Now making sure you are in Sync from the command line.

## Verify that your **remote origin** repository is the correct one 

Verify the the local copy of the repository has been copied from your personal fork.

To do so, type the following in the terminal window:

```bash
git remote -v
```
If you haven't changed directory into the repository directory -- you may get the following this rather frightening error:

```bash
/sbgenomics/workspace/adeslatt$ git remote -v
fatal: not a git repository (or any parent up to mount point /sbgenomics)
Stopping at filesystem boundary (GIT_DISCOVERY_ACROSS_FILESYSTEM not set).
```

But now if you simply *`cd`* into the proper directory.

```bash
cd exampleVolcanoPlotNotebook
```

You should see something like this:

```bash
origin  https://github.com/NIH-NICHD/exampleVolcanoPlotNotebook.git (fetch)
origin  https://github.com/NIH-NICHD/exampleVolcanoPlotNotebook.git (push)
```

## Add the initial repository from NIH-NICHD as your **remote upstream**

This will help us, if there are changes in the future in the initial repository, to be able to absorb them in our version and keep them in sync

```bash
git remote add upstream https://github.com/adeslatt/exampleVolcanoPlotNotebook.git
```

## Verify that your **remote upstream** repository is the correct one (the `adeslatt` one)

Now we verify that we have the main repository upstream

```bash
git remote -v
```

And we should see something like this.

```bash
origin  https://github.com/adeslatt/exampleVolcanoPlotNotebook.git (fetch)
origin  https://github.com/adeslatt/exampleVolcanoPlotNotebook.git (push)
upstream        https://github.com/NIH-NICHD/exampleVolcanoPlotNotebook (fetch)
upstream        https://github.com/NIH-NICHD/exampleVolcanoPlotNotebook (push)
```

## Bring the two relative repositories in sync

To do that we will use a variation of the command called `pull`, that pulls potential changes that exist in the remote version of the repository in GitHub in our local copy. 

```bash
git pull upstream main --ff-only
```

The flag `--ff-only` protects us from overwriting work that may be in conflict between the two remote versions.

## Update our own version under our GitHub name with latest changes from the initial repository

After retrieving all the potential changes that exist between our own personal forked repository with the initial repository under `NIH-NICHD` we can use the command `push` to update our version with latest changes. To do that, type:

```
git push

```

This will send the latest changes that were added in your local copy to your forked repository. 

You will be prompted to authenticate giving your username and password in the terminal.

Which no longer works this way -- and we need to authenticate with our authentication token.

## Return to Day 2

[Return to Day 2](day-2-code-versioning.md)

