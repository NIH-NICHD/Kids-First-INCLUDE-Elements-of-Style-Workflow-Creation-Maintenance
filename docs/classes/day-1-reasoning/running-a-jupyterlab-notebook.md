
<img src="/../../img/JupyterLabLogoWithName.png"  width="250">

To begin, your screen should look like this:

<img src="/../../img/CAVATICAJupyterLabNotebookStartupScreen.png" width=650>

This is a [JupyterLab](https://jupyter.org) environment.  Project Jupyter is a non-profit, open-source project, born out of the IPython Project in 2014 as it evolved to support interactive data science and scientific computing across all programming languages. Jupyter will always be 100% open-source software, free for all to use and released under the liberal terms of the modified BSD license. 

<img src="/../../img/JupyterProjectAbout.png" width=650>

I encourage you to explore Project Jupyter and understand the directions they are going in and how they support open, transparent, re-purposeable and literate programming.  

The JupyterLab Notebook environment supports at this point 40 languages, in kernels, providing a flexible way to achieve not only the ends of what we are trying to do with analysis, but in a well documented, clear and literate manner.

<img src="/../../img/JupyterLabTheClassicNotebookForLiterateProgramming.png" width=650>

Now that we are at the terminal window, we need to bring our lesson in hand -- and to do that, we are going to begin with *`forking`* our *`GitHub`* repository.

## Clone a GitHub Repository

We are going to clone a GitHub repository - to do so navigate in your browser to [Example Volcano Plot Notebook](https://github.com/NIH-NICHD/exampleVolcanoPlotNotebook)

<img src="/../../img/exampleVolcanoPlotCodeClone.png" width = 500>

## Copy the Link to Clone the repository

Next, navigate to the 🟦`Code` button on the right and select `HTTPS` and copy the link.

## Clone the repository in the Jupyterlab terminal window

Return to your CAVATICA Window and go back to your JupyterLab notebook.
And select the `terminal window`

<img src="/../../img/cloneExampleVolcanoPlotNotebook.png" width=500>

Now we want to clone the repository fork we made:

At the prompt type:

```bash
git clone https://github.com/NIH-NICHD/exampleVolcanoPlotNotebook.git
```

Now let's use our *`cd`* command to change into the appropriate directory.

```bash
cd exampleVolcanoPlotNotebook
111

### Open the `Reading-data-and-plotting-in-R.ipynb`

Next, we will execute the second `jupyterlab` notebook, this one is running the `R` kernel.

Look again at the folders on the left and open the second notebook `Reading-data-and-plotting-in-R.ipynb` by double-clicking on the notebook.

<img src="https://github.com/NIH-NICHD/Kids-First-Elements-of-Style-Workflow-Creation-Maintenance/blob/main/assets/CAVATICAJupyterLabNotebook2-ReadingDataAndPlottingR.png">

Again, `Restart Kernel and Clear Outputs`.

<img src="https://github.com/NIH-NICHD/Kids-First-Elements-of-Style-Workflow-Creation-Maintenance/blob/main/assets/CAVATICAJupyterLabNotebook2-RestartKernelAndClearOutputs.png">

Confirm your desire to do so:

<img src="https://github.com/NIH-NICHD/Kids-First-Elements-of-Style-Workflow-Creation-Maintenance/blob/main/assets/CAVATICAJupyterLabNotebook2-RestartKernalConfirmation.png">

This is running the `R` Kernel and as we load the libraries we see that there is a `[*]` inside the brackets.   This indicates that it is executing and looks like this:

<img src="https://github.com/NIH-NICHD/Kids-First-Elements-of-Style-Workflow-Creation-Maintenance/blob/main/assets/CAVATICAJupyterLabNotebook2-RWaitingUntilCompletion.png">

When completed, it will look the `[*]` becomes `[1]`.

## Recap

In this lesson:
* We logged into CAVATICA
* We started an interactive analysis with JupyterLab
* We authenticated with GitHub
* We executed and saw some Command Line Functions
* We generated a Volcano Plot in a JupyterLab notebook running an `R` kernel


## Return to the Agenda

[Agenda for the Day 1: Reasoning](https://github.com/NIH-NICHD/Kids-First-Elements-of-Style-Workflow-Creation-Maintenance#agenda-for-the-day-1-reasoning)

## Additional resources:

- CAVATICA documentation for the JupyterLab interface: https://docs.cavatica.org/docs/editor-quick-reference
- Official documentation from project JupyterLab: https://jupyterlab.readthedocs.io/en/stable/ 
