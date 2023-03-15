## Let's return to our exampleVolcanoPlot

On our first day, the notebook we started had an error.

Day 1
- Introduced _The Elements of Style_ approach
- On-boarded to the _Cavatica_ platform and started _Data Studio_ which is a _JupyterLab Notebook_
- Inspected the _exampleVolcanoPlot.ipynb_ which is a _JupyterLab Notebook_ running an _R_ Kernal

Day 2
- Introduced the concepts of _Git_, _GitHub_
- Learned about _version control_, _attributions_, and how _GitHub_ enables a _Lab Notebook_ concept, preparing us to better use the vast and amazing capabilities available to us in a _managed platform_ environment with access to enormous power and storage via _Elastic Compute_ and the growing resources available on the cloud.
- We _Forked_ a repository
- We _Synced_ a repository
- We made a _pull request_.

## (optional) Run the Volcano plot

There were two missing steps to successfully run the [exampleVolcanoPlot](https://github.com/NIH-NICHD/exampleVolcanoPlotNotebook).

The *`Reading-data-and-plotting-in-R.ipynb`*, a _JupyterLab Notebook_ running an _R_ kernal needed three items:

- the data found in _Zenodo_ at the _DOI (Data Object Identifier)_ location `*[https://doi.org/10.5281/zenodo.7510587](https://doi.org/10.5281/zenodo.7510587)*`.
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

[Return to the Agenda](day-3-containerizing.md)