# Lab Report 4: Editing using vim, and pushing changes to Git
## Step 4: Log onto ieng6
Because I previously generated an SSH key for ieng6, I do not need to enter my password. 
I typed in: `ssh cs15lsp23rd@ieng6.ucsd.edu` into the command-line and pressed `<enter>`to log in. 

The ssh command allows me to connect remotely to the ieng6 server, and the chunk of text after that is simply my course-specific account.
![Image](step4.png)

## Step 5: Clone your fork of the repository from your Github account
Because I previously generated an SSH key for GitHub as well, I can clone my fork of the repository from my Github account using the SSH link.

So, in order to do this, in the command-line, I type in `git clone git@github.com:xArthurCheungx/lab7.git` and subsequently press `<enter>`
![Image](step5.png)

## Step 6: Run the tests, demonstrating that they fail
To run the the tests, we first need to compile them. 
So, I first type in `cd lab7` and press `<enter>` to change my working directory to the lab7 directory we want to work with (the one we just cloned). 
Then, I type in `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` and press `<enter>`. This command essentially compiles the Tester and ListExamples java files as well as the JUnit jar files. 
Now, to actually run the tests, I use the `java` command to run the files containing the tests. So, I type in <br> `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests` 
## Step 7: Edit the code file to fix the failing test
## Step 8: Run the tests, demonstrating that they now succeed
## Step 9: Commit and push the resulting change to your Github account

