# Workspace Set-up
<br/><br/>

Today, we will start either with the JupyterLab Notebook you started yesterday or if you have not already registered and started a JupyterLab Notebook, please go ahead and do so.

For the class, we recommend you use the Chrome Browswer.   And as you click through the lesson, open each link in a new tab.

## Already had a notebook yesterday

_Navigate_ to [CAVATICA](https://cavatica.sbgenomics.com) and go ahead and *`log in`*.

You will land at a Dashboard, on the left you have your projects, and on your right your analyses.

<img src="/../../img/CAVATICAWorkspaceSetupDashboard.png" width=650>

### Select *`Data Studio`*

You will see all your past analyses.   _Note that you do not pay for your analyses when they are stopped._ You also see documentation regarding the environment you had set up, the cost and the duration spent on the session.

<img src="/../../img/CAVATICAWorkspaceDataStudioPastSavedAnalyses.png" width=650>

You will also see *`Files`* and *`Settings`*.   You **Do** pay for storage.   The [Cloud Cost Overview](https://github.com/kids-first/kf-cloud-credits#readme) the Kids First DRC helps you calculate costs.  

### Files

Lets look at Files.

<img src="/../../img/CAVATICAWorkspaceDataStudioFilesOutputsPicture.png" width=650>

In general, adopting a habit of getting in to do your work, developing your analysis and your workflows in small pieces with small files before you execute over 100s if not 1000s of files, will save you time and money.   

Be judicious in what files you need to keep.  This is a habit that will save you.   

This is why we use GitHub, we deposit our original measurement data in appropriate public storage sites.  We use repositories such as Zenodo for Data Object Identifiers and GitHub to track our Notebooks, which are essentially our scientific electronic notebooks, and our workflows.

### Settings

Here you have the opportunity to change the size of your machine.   If you scroll down, you will see the size and the price of the machine.

<img src="/../../img/CAVATICAWorkspaceDataStudioSettingsPicture.png" width=650>

One thing to note.  We are using a *`dedicated`* instance when we are doing interactive analysis.   That is why the price is $0.34/hour.   When we run a workflow, we typically use *`spot`* instances that are usually 1/8th the cost or so.  This then allows us to *`Fire and Forget`*.  The beauty of *`spot`* instances is not only are they cheaper, but they help enforce that they are ephemeral, that is from a security, cost standpoint they are ideal.  They exist, their images loaded onto them and then they are gone.   This is why we always run workflows that are in GitHub and/or an App that is persistent.  The memory of what was run is held in the repository.  So when you publish, or you collaborate, or when you ship your analyses or your workflow to a collaborator, you can share the repository, making configuration adjustments for platform differences within the repository.

More on that later.

## Start your notebook.

Go ahead and hit <img src="/../../img/CAVATICAWorkspaceDataStudioStartButton.png" width=50> and lets get started.

Give us a <img src="/../../img/thumbsup.png" width=50> in the Zoom chat if all is going ok. 

<img src="/../../img/CAVATICAWorkspaceDataStudioInstanceStartingPicture.png" width=650>

You will soon see the JupyterLab Launch pad - which as we know will stay alive for about 30 minutes.

<img src="/../../img/CAVATICAWorkspaceDataStudioJupyterLabNotebookLaunchPad.png" width=650>

Lets go back to the lesson and understand a bit about [Why Git and GitHub](why-git-and-setup.md#a-why-git-and-github.md).

## Starting From Scratch

If you were not with us yesterday, please follow these directions to start a notebook.   If you need help, we will help you at the coffee break or reach out to David in the Chat.

## Continue with our Lesson for Day 2 

[Return to Agenda](day-2-code-versioning.md)
