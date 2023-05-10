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


