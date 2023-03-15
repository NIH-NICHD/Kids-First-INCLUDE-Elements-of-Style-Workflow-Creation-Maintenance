## Let's Recap

Day 1

- Introduced _The Elements of Style_ approach
- On-boarded to the _Cavatica_ platform and started _Data Studio_ which is a _JupyterLab Notebook_
- Inspected the _exampleVolcanoPlot.ipynb_ which is a _JupyterLab Notebook_ running an _R_ Kernal

Day 2

- Introduced the concepts of _Git_, _GitHub_
- Learned about _version control_, _attributions_, and how _GitHub_ enables a _Lab Notebook_ concept, preparing us to better use the vast and amazing capabilities available to us in the _managed platform_ environment, _Cavatica_ with access to enormous power and storage via _Elastic Compute_ and the growing resources available on the cloud.
- We _Forked_ a repository
- We _Synced_ a repository
- We made a _pull request_.

## Let's revisit _Reading Data and Plotting in R_

There were two missing steps to successfully run the [exampleVolcanoPlot](https://github.com/NIH-NICHD/exampleVolcanoPlotNotebook).

The *`Reading-data-and-plotting-in-R.ipynb`*, a _JupyterLab Notebook_ running an _R_ kernal needed three items:

- the data found in _Zenodo_ at the _DOI (Data Object Identifier)_ location [https://doi.org/10.5281/zenodo.7510587](https://doi.org/10.5281/zenodo.7510587).
- to have run the command to install required dependencies on the machine where the notebook was running `*rscript install_dependencies.R*`.
- and finally to declare one of the libraries installed that was not yet declared: `*library(rlang)*`.

Those changes were updated in the original repository [https://github.com/adeslatt/exampleVolcanoPlotNotebook](https://github.com/adeslatt/exampleVolcanoPlotNotebook).

And if you have synchronized with the repository you _Forked_ your repository from [https://github.com/NIH-NICHD/exampleVolcanoPlotNotebook](https://github.com/NIH-NICHD/exampleVolcanoPlotNotebook), your repository is now up-to-date.


### Let's Read Data and Plot in R !

Go ahead and hit <img src="/../../img/CAVATICAWorkspaceDataStudioStartButton.png" width=50> and lets get started.

Give us a <img src="/../../img/thumbsup.png" width=50> in the Zoom chat if all is going ok. 

<img src="/../../img/CAVATICAWorkspaceDataStudioInstanceStartingPicture.png" width=650>

You will soon see the JupyterLab Launch pad - which as we know will stay alive for about 30 minutes.

<img src="/../../img/CAVATICAWorkspaceDataStudioJupyterLabNotebookLaunchPad.png" width=650>

## Navigate to the right directory

From the _command line_, navigate to the location where you _git clone_'d your personal _fork_ of the _NIH-NICHD_ repository.

```bash
cd adeslatt
```

<img src="/../../img/RecapCDPersonal1.png" width=650>

Now check the status of the repository with the command _git status_

```bash
git status
```

Uh-oh there is a problem!

<img src="/../../img/RecapUhOhFatalError2.png" width=650>

That's ok we were not quite in the right directory.

You can look around where you are by using a command we learned yesterday _ls -l_

```bash
ls -l
```

Let's go down one more level to where the stuff we checked out of the repository actually is:

```bash
cd exampleVolcanoPlotNotebook
```

<img src="/../../img/RecapCDGitHubCorrectDirectory3.png" width=650>

To check the status and to check the difference between what is in your directory and what is stored in your repository you use two commands _git status_ and _git diff_

```bash
git status
```

followed by

```bash
git diff
```

<img src="/../../img/RecapGitStatusGitDiff4.png" width=650>

Now in my case the repository had its own changes, but when I looked at the repository on the web site, they were identical.  So I have decided I simply want to remove this directory with this work.   I know it seems scary to do that, but with my changes in GitHub I have nothing to worry about.

We are going to use another new command _cd .._.  In a terminal window there are shortcuts.  Programmers like to use as few characters as possible to accomplish their work, including moving around in a terminal window.  Over time you will also not only grow accustomed to these handy short cuts, but you will enjoy them as well.

To look at your current directory you can use *`.`*.   To look at the parent directory (what we call the directory above the one we are in, you can use *`..`*.

Go ahead and look around your current directory, by typing the unnecessary command _cd ._ but I am using it to demonstrate a point (ha-ha).

```bash
cd .
ls -l
```

But what we wanted to do is move up to the parent directoery.

```bash
cd ..
ls -l
```

<img src="/../../img/RecapCDToParentDirectory5.png" width=650>

Ok now I want to remove the entire directory.   Because I had local and changes at the master and really did not need to or desire to worry about how to clean it up.  Easiest is to wipe the slate clean and get a fresh copy.

We will use _rm_ together with the options _-f_ for force and _-R_ for recursively delete all the subdirectories inside as well.   You can go into [ExplainShell](https://explainshell.com/) to see this information for yourself.

I also will get my clean repository by going to the `code` button and getting a copy by copying with the right protocol, *`HTTPS*` the link for _git_ to use 

```bash
rm -f -R
git clone https://github.com/adeslatt/exampleVolcanoPlotNotebook.git
```

<img src="/../../img/RecapRMandCloneNew6.png" width=650>

Now again open the notebook.

<img src="/../../img/RecapOpenReadingDataAndPlottinginR7.png" width=650>

Clear the outputs and restart the Kernel.

<img src="/../../img/RecapClearOutputsRestartKernel8.png" width=650>

Confirm
<img src="/../../img/RecapConfirm9.png" width=650>

And re-run!

Now let's go back to our course.

[Return to the Agenda](day-3-containerizing.md)