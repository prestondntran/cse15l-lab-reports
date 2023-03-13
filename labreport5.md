# Lab Report 5: Redoing Lab Report 4

This report improves upon the completion time of the CS Labs Done Quick activity by using bash scripts.

## Part A: Setup for the Activity

### Step 1: Writing Bash Scripts (Before Editing ListExamples)

![Image](https://user-images.githubusercontent.com/86041345/224603891-28a4b17d-07d0-4f96-ae90-13241156ece9.png)

This first bash script, `before.sh`, serves to complete multiple steps in the activity. Each of the lines in
the script are taken from Lab Report 4: the first line clones the fork of the `lab7` repository, the next
command changes the current directory to `lab7`, the next one compiles the java files within this directory,
the next one runs the `ListExamplesTests` file, and the last command allows us to edit `ListExamples.java`.

### Step 2: Writing Bash Scripts (After Editing ListExamples)

![Image](https://user-images.githubusercontent.com/86041345/224605284-efa6a1a7-54a5-4680-a83f-df192b8a25c0.png)

After editing `ListExamples.java` appropriately, this second bash script, `after.sh`, completes the remaining 
steps in the activity. Each of the lines in the script are also taken from Lab Report 4 (with the exception 
of the first line, `cd lab7`, which ensures that we stay in the right directory to compile and run files). 
The same commands for compiling and running java files are used again, this time with the corrected 
`ListExamples.java` file. The remaining commands commit and push these changes.

### Step 3: Copying the Scripts to the Remote Server

![Image](https://user-images.githubusercontent.com/86041345/224605954-a59d4907-c94c-45bc-939d-acd741b047b2.png)

In order to use the bash scripts while working in the remote server, the `scp` command is used to copy them
into the remote server, as shown above. After this, the setup for the activity is complete.

## Part B: Doing the Activity

