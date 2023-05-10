# Lab Report 3: Interesting Command-line Options for grep
Note that for the examples below, I will already be in the `./technical` directory, and thus use relative paths to get to text files accordingly.
## Command Line Option 1: Count of Matches
The `$ grep -c [pattern] [file]` command allows us to see the number of matches/instances there are in the file, where `pattern` can be substituted for any string you want to find the count for, and `file` being the path for any text file.
### Example 1:
Input command: `grep -c Wolbachia plos/journal.pbio.0020068.txt`

Output: `11`
### Example 2:
Input command: `grep -c biodiversity plos/journal.pbio.0020406.txt` 

Output: `9`

In both examples, we see that that this command outputs the number of instances of the exact case-sensitive string (the first argument after the `-c`) in the file given (the second argument given after the `-c`).

So, we know that there are 11 times where `"Wolbachia"` is found in `journal.pbio.0020068.txt` file, and that there are 9 times where `"biodiversity"` is found in the `journal.pbio.0020406.txt` file. 

Similar to the `wc` command we learned in class, this option for `grep` can save time and effort when searching for specific patterns or counting the occurrences of particular words or phrases in files or logs.

### Source:
[16 grep Command Examples to Help You in Real-World - geekflare.com](https://geekflare.com/grep-command-examples/)

## Command Line Option 2: Inverse Search
The `$ grep -v [pattern] [file]` command finds and outputs all lines in the given text file that *don't* match the given pattern, where `pattern` can be substituted for any string you want to exclude in your search, and `file` being the path for any text file.
### Example 3:
Input command: `grep -v a 911report/chapter-2.txt`

Output: `
    
        
            THE FOUNDATION OF THE NEW TERRORISM
            A DECLARATION OF WAR
            
                these themes.
            
            
            
            BIN LADIN'S APPEAL IN THE ISLAMIC WORLD 
            
            
            
            
            
                nonbeliever worthy of destruction.
            
                support for their countries' repressive rulers.
                desire life."
            
            
            
            THE RISE OF BIN LADIN AND AL QAEDA (1988-1992)
            
            
            
            
            
            
                    circle.
            
            
            
            
            
            
            
            
            
            
                    well.
            
            
            
            
            
            BUILDING AN ORGANIZATION, DECLARING WAR ON THE UNITED STATES
                (1992-1996)
            
            
            
            
            
            
                    unknown.
            
                the cylinder, then discovered it to be bogus.
            
            
            
            
            
            
                    request.
            
                connections.
            
            
            
            
                    section.
            
            
            AL QAEDA'S RENEWAL IN AFGHANISTAN (1996-1998)
            
            
            
            
            
            
            
            
                    entirely.
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
        `
### Example 4:
Input command: `` 

Output: ``

In these examples,

### Source:
[16 grep Command Examples to Help You in Real-World - geekflare.com](https://geekflare.com/grep-command-examples/)

## Command Line Option 3: Match only Whole Words
The `$ grep -v [pattern] [file]` command 
### Example 5:
Input command: ``

Output: ``
### Example 6:
Input command: `` 

Output: ``

In these examples,

### Source:
[grep Command in Linux with Examples (Search for a pattern in a file) - Reddit(r/commandline)](https://www.reddit.com/r/commandline/comments/m14s0y/grep_command_in_linux_with_examples_search_for_a/)

## Command Line Option 4: Ignore Cases
The `$ grep -v [pattern] [file]` command 
### Example 7:
Input command: ``

Output: ``
### Example 8:
Input command: `` 

Output: ``

In these examples,

[grep Command in Linux with Examples (Search for a pattern in a file) - Reddit(r/commandline)](https://www.reddit.com/r/commandline/comments/m14s0y/grep_command_in_linux_with_examples_search_for_a/)



