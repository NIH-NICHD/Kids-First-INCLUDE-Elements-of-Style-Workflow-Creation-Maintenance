
## GitHub Authentication

To make a contribution to a GitHub repository, you need to authenticate.

You can do this with the tool we installed `gh`.

I didn't mention where I found this?   Yesterday I told you about [Anaconda Package Library](anaconda.org/anaconda/repo). There you can find an active contributor environment and the latest tools that can be used from the command line, in your containers and in your workflows.   It is as I mentioned an excellent place to educate and everyday working with these pacakges is easier and easier.

<img src="/../../img/Anaconda-conda-forge-gh.png" width=650>

Here we see that `gh` is the **GitHub CLI** where **CLI** stands for _**Command Line Interface**_, the application we now have been using for the last two days.

### Generating A GitHub Authentication Token

Before we _**authenticate**_ with _**GitHub**_ we need to generate a token that we will provide to _**GitHub**_ to tell that application who we are.  This is a _**Personal Access Token**_ your private secret key to prove who you are.

_**Step 1**_ - Navigate to Settings, located just under your profile in the upper right hand corner:

<img src="/../../img/GitHubGeneratePersonalAccessToken1.png" width=650>

_**Step 2**_ - Navigate to the bottom to `< > Developer Settings` on the bottom left hand corner:

<img src="/../../img/GitHubGeneratePersonalAccessToken2.png" width=650>

_**Step 3**_ - Select `Personal access tokens` third option from the top on the left side:

<img src="/../../img/GitHubGeneratePersonalAccessToken3.png" width=650>

_**Step 4**_ - Select `Generate new token` on the upper right corner - put a name in the note I used `eos`

<img src="/../../img/GitHubGeneratePersonalAccessToken4.png" width=650>

_**Step 5**_ - Select all of the options and select `Generate token`

<img src="/../../img/GitHubGeneratePersonalAccessToken5.png" width=650>

_**Step 6**_ - Copy the token because as the note mentions - it will not be available again - but you can regenerate tokens now - so don't worry.

<img src="/../../img/GitHubGeneratePersonalAccessToken6.png">

### Now we can authenticate with GitHub
Once we have our token, we can now authenticate.

_**Step 1**_ - _Type_ **gh auth login** at the command line in the **Terminal** window

<img src="/../../img/JupyterLabNotebookTerminalghauthlogin.png" width=650>

_**Step 2**_ - Use arrow keeps and select _GitHub.com_ (should be the default)

<img src="/../../img/JupyterLabNotebookTerminalSelectGitHub.png" width=650>

_**Step 3**_ - Select _HTTPS_ for your _preferred protocol for git operations

<img src="/../../img/JupyterLabNotebookTerminalSelectHTTPS.png" width=650>

_**Step 4**_ - Confirm you wish to authenticate with your GitHub Credentials

<img src="/../../img/JupyterLabNotebookTerminalConfirmGitHub.png" width=650>

_**Step 5**_ - Use arrow keys to select _Paste an authentication token_

<img src="/../../img/JupyterLabNotebookTerminalPasteAuthToken.png" width=650>

_**Summary of all the steps**_

<img src="/../../img/CAVATICAJupyterLabGHAuthLoginWithToken.png">

## [Return to Agenda](day-2-code-versioning.md) 
