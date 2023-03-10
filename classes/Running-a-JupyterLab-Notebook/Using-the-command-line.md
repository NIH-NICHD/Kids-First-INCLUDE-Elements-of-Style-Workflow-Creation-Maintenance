# Using the command line

Because I want to make this course accessible to researchers/clinicians who may or may not have had previous command line experience, I recently asked chatGPT the following question:


*how would you explain "what is a terminal window" and "what is a command line" to someone naive to these terms?*

**ChatGPT** had the following response

```bash

A terminal window is a type of computer program that allows you to interact with your computer using text commands instead of clicking on icons or menus with a mouse. It's a way to access the "guts" of your computer and execute specific instructions.

A command line is the text interface in a terminal window where you can enter these instructions or commands. Essentially, it's a way to communicate with your computer using a language that it understands. Instead of pointing and clicking with a mouse, you type out specific commands to make things happen.

For example, if you want to create a new folder, you could type "mkdir foldername" in the command line, and the computer would create a new folder with the name you specified. Or if you want to open a specific program, you could type its name followed by ".exe" and press enter, and the program would launch.

The command line can be a powerful tool for accomplishing tasks quickly and efficiently, but it does require some knowledge of specific commands and syntax. However, there are many resources available online for learning how to use the command line, and many people find it to be a valuable skill to have.

```
x. However, there are many resources available online for learning how to use the command line, and many people find it to be a valuable skill to have.~
Maybe before we begin with using the One of the barriers to getting started in creating ones own workflows, or even navigating and using simple tools for inspecting files, is understanding to do so requires understanding that there is a terminal window within which you can 
Useful commands to perform programmatically common operations over files and folders (create, copy, move, delete, download or navigate folders)


## Utilising the ExplainShell interactive command explorer

There is an excellent resource that provides an interactive command explainer that can be accessed at https://explainshell.com/.
Feel free to use and paste the following commands from the tutorial to see an explanation of the command based on the official commands documentation.



## 1. List files in the current folder 

Directory is used interchangeably with the term folder.

```bash
ls -l
```

## 2. Inspect your current folder location in the file system

To see in which folder you are currently in, use the **`pwd`** command, short fro **`print working directory`**. This will return the absolut path to the location you currently stand.

> NOTE: 
What is an _absolut_ path? And what is not considered an absolut path?

See this resource for a thorough explanation: https://linuxfoundation.org/blog/classic-sysadmin-absolute-path-vs-relative-path-in-linux-unix/

```bash
pwd
```

## 3. Copy a file

Duplicate the file content while retaining the initial copy

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

## 6. Delete a folder

We can delete a folder using the `rm -r` command:

```bash
rm -r new_folder
```

Let's inspect that the folder is indeed deleted:

```bash
ls -l
```

<!-- #region -->
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

<!-- #endregion -->

```bash

```
