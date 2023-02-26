# Lab Report 4: CSE Labs Done Quick

## Step 1: Log Into ieng6

![Image](https://user-images.githubusercontent.com/86041345/221394190-80da68d9-17f1-4c17-8451-a93e021bcb6c.png)

Keys pressed: `ssh <up><enter>`
  
I typed out `ssh`, and I saved time by pressing the up key once to access
my ieng6 address instead of typing the whole address out.
  
## Step 2: Clone the Fork
  
![Image](https://user-images.githubusercontent.com/86041345/221394342-bc58afbd-0f5c-4fe0-bed6-3733926aa9fa.png)  
  
Keys pressed: `git clone <command+v><enter>`
  
I typed out `git clone`, and I pasted the link to the fork of the repository
by pressing command and v. (During the set up phase, I pressed the copied
button in GitHub to copy the fork's link.)

## Step 3: Run the Incorrect Tests

![Image](https://user-images.githubusercontent.com/86041345/221394843-8f618fd1-8b8b-46bc-9dae-b1c595d7eab5.png)

Keys pressed: `cd l<tab><enter>`, `<control+r>j<enter>`, `<control+r>java <enter>`

First, I typed `cd l` and pressed tab to autocomplete to `lab7` in order to
enter the lab7 directory. To compile the java files, I pressed control and r 
to search through my command history. I typed j and `javac -cp .:lib/hamcrest
-core-1.3.jar:lib/junit-4.13.2.jar *.java` appeared. After compiling, I ran
the tester file by pressing control and r again, followed by typing `java `
(including the space after `java`) so that `java -cp .:lib/hamcrest-core-1.3.
jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests` appears.

## Step 4: Edit the Code

![Image](https://user-images.githubusercontent.com/86041345/221395128-a223450f-a71e-452b-905d-3eb2beedf3c1.png)

Keys pressed: `nano L<tab>.j<tab><enter>`, `<control+v><up x 7><right x 12>`,
`<backspace>2`, `<control+o><enter><control+x>`

To edit the `ListExamples.java` file, I typed `nano L` followed by the tab key
and then `.j` followed by the tab key. Each tab autocompletes so that the file
name shows up. Once I enter the file editor, I press control and v to skip to
the bottom of the file. Then, I press up 7 times and right 12 times to get to
the code that needs to be edited. I press backspace and 2 to fix the code, I
press control and o to save my edits, and I press control and x to exit editing.

## Step 5: Run the Fixed Tests

![Image](https://user-images.githubusercontent.com/86041345/221395372-e405dc0f-5b67-41c1-87d0-28f3cdefc774.png)

Keys pressed: `<up><up><up><enter>`, `<up><up><up><enter>`

To compile the code once more, I pressed the up key three times to locate
`javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` in my
command history. To run the code, I also pressed the up key three times to
access `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.
runner.JUnitCore ListExamplesTests`.

## Step 6: Commit and Push

![Image](https://user-images.githubusercontent.com/86041345/221395546-e652e48a-9f89-47f3-9d8c-a3ccebfeef4a.png)

Keys pressed: `git add L<tab>.j<tab><enter>`, `git commit -m "Updated"`,
`git push`

First, I typed `git add L` followed by the tab key and then `.j` followed by
the tab key. As discussed earlier, the tabs serve to autocomplete the file name.
To commit, I typed `git commit -m "Updated"`; to push, I typed `git push`.
