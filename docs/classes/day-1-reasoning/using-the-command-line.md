# Using the command line

Because I want to make this course accessible to researchers/clinicians who may or may not have had previous command line experience, I recently asked chatGPT the following question:


*how would you explain "what is a terminal window" and "what is a command line" to someone naive to these terms?*

**ChatGPT** had the following response


> A terminal window is a type of computer program that allows you to interact with your computer using text commands instead of clicking on icons or menus with a mouse. It's a way to access the "guts" of your computer and execute specific instructions.
>
>A command line is the text interface in a terminal window where you can enter these instructions or commands. Essentially, it's a way to communicate with your computer using a language that it understands. Instead of pointing and clicking with a mouse, you type out specific commands to make things happen.
>
>For example, if you want to create a new folder, you could type "mkdir foldername" in the command line, and the computer would create a new folder with the name you specified. Or if you want to open a specific program, you could type its name followed by ".exe" and press enter, and the program would launch.
>
The command line can be a powerful tool for accomplishing tasks quickly and efficiently, but it does require some knowledge of specific commands and syntax. However, there are many resources available online for learning how to use the command line, and many people find it to be a valuable skill to have.
>
>However, there are many resources available online for learning how to use the command line, and many people find it to be a valuable skill to have.


We begin by using a tool [ExlainShell](https://explainshell.com/)


## Utilising the ExplainShell interactive command explorer

There is an excellent resource that provides an interactive command explainer that can be accessed at [ExplainShell](https://explainshell.com/)
Feel free to use and paste the following commands from the tutorial to see an explanation of the command based on the official commands documentation.


## 1. List files in the current folder 

Directory is used interchangeably with the term folder.

```bash
ls -l
```

Inside [ExplainShell](https://explainshell.com/) you will see the following explanation:

<img src="/../../img/ExplainShell_ls_l.png" width=500>

## 2. Inspect your current folder location in the file system

To see in which folder you are currently in, use the **`pwd`** command, short for **`print working directory`**. This will return the absolut path to the location you currently stand.

> NOTE: 
What is an _absolute_ path? what is a _relative_ path? 

[See this resource for a thorough explanation](https://linuxfoundation.org/blog/classic-sysadmin-absolute-path-vs-relative-path-in-linux-unix/)

Again feel free now to copy and paste this command in the [ExplainShell](https://explainshell.com)

```bash
pwd
```

<img src="/../../img/ExplainShellpwd.png" width=500>


## 3. Copy a file

Now let's go to a terminal window inside of the JupyterLab notebook you have just started up.

Select terminal

<img src="/../../img/JupyterLabNotebookSelectTerminalWindow.png" width=500>

Then you will see the command-line:

<img src="/../../img/JupyterLabNotebookCommandLine.png" width=500>

Before we copy a file, let's use a command-line command *`echo`* and create a file with the content "I am the header of your first README.md".

If you want to know about this command, look it up on [ExplainShell](https://explainshell.com).

We are also using a command called a *`redirect`* -- this will use it to put content into a new file.

```bash
echo 'I am the header of your first README.md' > README.md
```

You can run `ls -l` to see that the file is there.  As well as see the commands *`more`* and another command called *`less`*.

Use [ExplainShell](https://explainshell.com) to know about these commands, but they show the contents of the file as you might expect.

<img src="/../../img/JupyterLabNotebookTerminalWindowEchoToCreateAREADME.md.png" width = 500>

Now let's create a copy:

```bash
cp README.md duplicated_README.md
```

Now let's inspect if the file was created, by listing files in the directory with the `ls -l` command. We are expecting to view the file with name `duplicated_README.md` in the listed files and folders

```bash
ls -l
```

# 4. Deleting a file

To delete (remove) a file we can use the command `rm name_of_folder`. Let's delete the duplicate README.md file named `duplicated_README.md`


```bash
rm duplicated_README.md
```

Now let's inspect if the file was created, by listing files in the directory with the `ls -l` command. We are expecting to **not** view the file with name `duplicated_README.md` as we just **deleted** it in the listed files and folders

```bash
ls -l
```

## 5. Create a new directory (folder)

To create a new folder if that folder doesn't exist, we can use the command `mkdir name_of_folder`. Let's create a folder named `new_folder`



```bash
mkdir new_folder
```

Now let's inspect if the folder was created, by listing files in the directory with the `ls -l` command. We are expecting to view the folder with name `new_folder` in the listed files and folders


Let's inspect the folder exists with our trusted `ls -l` command

```bash
ls -l
```

<img src="/../../img/JupyterLabNotebookNewFolderAndContent.png" width=500>

## 6. Delete a folder

We can delete a folder using the `rm -r` command:

```bash
rm -r new_folder
```

Let's inspect that the folder is indeed deleted:

```bash
ls -l
```


## 7. Downloading a file using a link

We can retrieve a file using a public link. For example, we have uploaded in a public ZENODO record for this course an example file. The link for the file is: https://zenodo.org/record/4302133/files/deseq2_5k.csv

Details of this file, which is a selected subset of the results of running DESeq on RNA-seq files, only those that were with an appropriate p-value (< 0.05) and above the 1.5 fold difference were put into the matrix.   

https://zenodo.org/record/4302133.   You can see the version history, this file was created by a colleague at Lifebit, for the first time this course was offered in 2019 at the Jackson Laboratory.

To retrieve this file, we are going to open the terminal window and run the command:

```bash
cd /sbgenomics/workspace/Kids-First-Elements-of-Style-Workflow-Creation-Maintenance/classes/Running-a-JupyterLab-Notebook
wget https://zenodo.org/record/4302133/files/deseq2_5k.csv
```

So please copy this command and paste it in the terminal window and press return - in preparation for the next section of todays class.  Reading data and plotting a volcano plot.

## Return to Day 1 

[Return to today's agenda](day-1-reasoning.md)
