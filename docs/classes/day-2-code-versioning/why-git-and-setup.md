# Why Git and GitHub? 

Motivation and set up in the JupyterLab workspace


## Why Git? 

<img src="https://git-scm.com/images/logos/downloads/Git-Logo-1788C.png"  width="100">

Git is a [technology or a system used for version control](https://git-scm.com/) of code

- Frees up our code from our local machine (no risk of losing files from your laptop!)
- Ensures that we are tracking the changes of our code as a project progresses
- Allows us to revisit older versions of our code
- Allows us to keep different versions of our code

## Why GitHub?

<img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQGO2P0vFlvhsDbmltsjjIWZMi1dQCduIkuwA&usqp=CAU"  width="50"> 

Git **_Hub_** is a [_"code hosting platform for version control and collaboration"_](https://guides.github.com/activities/hello-world/)

- Large community of open source project to browse
- Enables collaboration of many contributors in the same project
- Serves as a code vault for making our reasearch code findable and our methods transparent


## Setting up in the terminal


## Using the `nano` file editor 

Before we start working with Git in the command line, we will learn one more helpful skill. How to use a code editor. A code editors allows us to edit files in an environment without a graphical user interface. For us, it will be needed in some Git related tasks, so we want to be prepared.

<!-- #region -->
Edit a file using nano in only 4 steps:

### 1. Type **`nano hello.txt`** 

This will create a new file named `hello.txt`. If the file already exists, it will open the file.

### 2. Write inside the open file named `hello.txt` 
As you typically would type in any Document editor eg Google Docs. You can type for example, `Hello Git!`

### 3. When ready to save type the shortcut:

<kbd> **`CTRL`**  </kbd> `+`  <kbd> **`O`** </kbd>

This will declare your willingness to save the file. Click <kbd> **`ENTER`**  </kbd> to verify that you want to save the file.

### 4. Close the file and exit from nano with the the shortcut:

<kbd> **`CTRL`**  </kbd> `+`  <kbd> **`X`** </kbd>

Awesome, your file has just been saved! You can inspect using the `head` command, eg `head hello.txt`

We will probably need soon `nano` in one of our Git tasks.

## Creating an environment to install packages

Not exactly required as the base environment within CAVATICA JupyterLab is already there.
But as a habit I begin with creating an environment so that I can keep track of what I add.

```bash
conda create -n eos -y
```

Once the environment is created, you activate it as instructed

```bash
conda activate eos
```

Then I install two additional things that I use on a regular basis, `GitHub CLI` and `emacs`

```bash
conda install -c conda-forge gh -y
```

### (Optionally install emacs) 

```bash
conda install -c conda-forge emacs -y
```

More on [*`Anaconda`*](https://anaconda.org/anaconda/repo) and packages later.

### Generating A GitHub Authentication Token

Step 1 - Navigate to Settings, located just under your profile in the upper right hand corner:

<img src="/../../img/GitHubGeneratePersonalAccessToken1.png" width=650>

Step 2 - Navigate to the bottom to `< > Developer Settings` on the bottom left hand corner:

<img src="/../../img/GitHubGeneratePersonalAccessToken2.png" width=650>

Step 3 - Select `Personal access tokens` third option from the top on the left side:

<img src="/../../img/GitHubGeneratePersonalAccessToken3.png" width=650>

Step 4 - Select `Generate new token` on the upper right corner - put a name in the note I used `eos`

<img src="/../../img/GitHubGeneratePersonalAccessToken4.png" width=650>

Step 5 - Select all of the options and select `Generate token`

<img src="/../../img/GitHubGeneratePersonalAccessToken5.png" width=650>

Step 6 - Copy the token because as the note mentions - it will not be available again - but you can regenerate tokens now - so don't worry.

<img src="/../../img/GitHubGeneratePersonalAccessToken6.png">

### Now we can authenticate with GitHub

Once we have our token, we can now authenticate.

<img src="/../../img/CAVATICAJupyterLabGHAuthLoginWithToken.png">

## Configuring our GitHub user information

To be able to use Git and GitHub from the command line we need to configure the information related to our GitHub user. Let's follow the commands below to set in the workspace the required information.

###  Set user _**name**_

Replace *`<my github user name>`* with your actual GitHub email.

```bash
git config --global user.name <my github user name>
```

### Set user _**email**_

Replace *`<my email associated with my github user name>`* with your actual GitHub email.

```bash
git config --global user.email <my email associated with my github user name>
```

### (Optional) Set preferred file editor eg _**nano**_ or _**emacs**_

```bash
git config --global core.editor nano
```

Or if you like *`emacs`*, or *`vim`*, change it to your desired *`editor`*.

```bash
git config --global core.editor emacs
```

