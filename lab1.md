# Lab Report 1 
Note: I have adapted this tutorial to Mac users only as I only have access to a Macbook.
## First step: Downloading & Installing Visual Studio Code
* Visit the visual studio code [website](https://code.visualstudio.com/, ), click the download button on the top right of the website, and download the version for macOS.
* After downloading, run the installer. 
* Once it has been installed, run the program and it should open up a window that looks like this (Ignore the files on the side; if it is newly installed, there should be no files on the side) : ![Image](VSCodeSS.png)

## Second step: Connecting to a Remote Server
* Now that we have access to an IDE (Integrated Development Environment), we can access a terminal that allows us to connect to a remote server. 
* However, we need to establish a password for our course-specific account for CSE15L so that we can access the remote server using our own accounts. To do this, click [this link](https://sdacs.ucsd.edu/~icc/index.php).
* On this website, you should see an account lookup section that looks like this: ![Image](AccountLookupSS.png)
* Enter your username (your UCSD email without the @ucsd.edu) and your Student ID (the ID you use for exams//the ID at the back if your Student ID card), and click Submit.
* You should then be taken to a website that looks like this ![Image](AccountLookupResultsSS.png) (Note that your username may be different to mine, and that your account name will be "cse15l" followed by a string of 4 characters that represent what quarter we are currently in, and subsequently two additional strings that *are unique to you*.) 
* Remember/note down your account name (the string that starts with "cse15l", not your UCSD username).
* Click the "UC San Diego Active Directory (AD) Password Change Tool" link on the website, and change your password to anything of your liking (though it is best to be secure).
* Now, we can go back to VS code and open a new terminal using the menu bar at the top (Terminal -> New Terminal). 
* You should now see something like this: ![Image](VSCodeTerminalSS.png)
* Click anywhere in the terminal, and type the following command: ssh cs15lsp23zz@ieng6.ucsd.edu. Replace the "zz" in this line with your own account name you noted down from before, and press enter.
* If the terminal asks the following question: "Are you sure you want to continue connecting (yes/no/[fingerprint])?", simply type yes and press enter.
* The terminal should then prompt a password like this: ![Image](PasswordPromptSS.png)
* Type the password you just recently set, and press enter. If you entered your password correctly you should then see this in the terminal: ![Image](SuccessfulLoginSS.png)
* Congratulations! You are now connected to the UCSD CSE15L remote server. This is where the fun begins!
## Third step: Traversing a Filesystem using commands
* 


