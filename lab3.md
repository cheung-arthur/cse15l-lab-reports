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

Output: 
```    
        
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
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
```
### Example 4:
Input command: `grep -v We 911report/preface.txt` 

Output: 
```
    
        
            PREFACE
                the President of the United States, the United States Congress, and the American
                people for their consideration. Ten Commissioners-five Republicans and five
                Democrats chosen by elected leaders from our nation's capital at a time of great
                partisan division-have come together to present this report without dissent.
                September 11, 2001, was a day of unprecedented shock and suffering in the history of
                the United States. The nation was unprepared. How did this happen, and how can we
                avoid such tragedy again?
            To answer these questions, the Congress and the President created the National
                Commission on Terrorist Attacks Upon the United States (Public Law 107-306, November
                27, 2002).
            Our mandate was sweeping. The law directed us to investigate "facts and circumstances
                relating to the terrorist attacks of September 11, 2001," including those relating
                to intelligence agencies, law enforcement agencies, diplomacy, immigration issues
                and border control, the flow of assets to terrorist organizations, commercial
                aviation, the role of congressional oversight and resource allocation, and other
                areas determined relevant by the Commission. In pursuing our mandate, we have
                reviewed more than 2.5 million pages of documents and interviewed more than 1,200
                individuals in ten countries. This included nearly every senior official from the
                current and previous administrations who had responsibility for topics covered in
                From the outset, we have been committed to share as much of our investigation as we
                can with the American people. To that end, we held 19 days of hearings and took
                public testimony from 160 witnesses.
            Our aim has not been to assign individual blame. Our aim has been to provide the
                fullest possible account of the events surrounding 9/11 and to identify lessons
                learned.
                enemy rallies broad support in the Arab and Muslim world by demanding redress of
                political grievances, but its hostility toward us and our values is limitless. Its
                purpose is to rid the world of religious and political pluralism, the plebiscite,
                and equal rights for women. It makes no distinction between military and civilian
                targets. Collateral damage is not in its lexicon.
                and national security did not understand how grave this threat could be, and did not
                fault lines within our government-between foreign and domestic intelligence, and
                sharing information across a large and unwieldy government that had been built in a
                different era to confront different dangers.
            At the outset of our work, we said we were looking backward in order to look forward.
                positive-an America that is safer, stronger, and wiser. That September day, we came
                together as a nation. The test before us is to sustain that unity of purpose and
                the long haul, to attack terrorists and prevent their ranks from swelling while at
                think about the way our government is organized. The massive departments and
                agencies that prevailed in the great struggles of the twentieth century must work
                together in new ways, so that all the instruments of national power can be combined.
                Congress needs dramatic change as well to strengthen oversight and focus
                accountability.
            As we complete our final report, we want to begin by thanking our fellow
                together over every page, and the report has benefited from this remarkable
                of our colleagues, as well as our great affection for them.
                Philip Zelikow, has contributed innumerable hours to the completion of this report,
                setting aside other important endeavors to take on this all-consuming assignment.
                They have conducted the exacting investigative work upon which the Commission has
                built. They have given good advice, and faithfully carried out our guidance. They
                officials, past and present, who were generous with their time and provided us with
                insight. The PENTTBOM team at the FBI, the Director's Review Group at the CIA, and
                Inspectors General at the Department of Justice and the CIA provided great
                of several previous Commissions, and we thank the Congressional Joint Inquiry, whose
                documents and witnesses, and the Government Printing Office and W.W. Norton
                & Company for helping to get this report to the broad public.
                whose persistence and dedication helped create the Commission. They have been with
                us each step of the way, as partners and witnesses. They know better than any of us
                the importance of the work we have undertaken.
                most complete account we can of the events of September 11, what happened and why.
                This final report is only a summary of what we have done, citing only a fraction of
                the sources we have consulted. But in an event of this scale, touching so many
                every knowledgeable person or found every relevant piece of paper. New information
                understanding of a landmark in the history of our nation.
                have admired their determination to do their best to prevent another tragedy while
                enormous sympathy for the victims and their loved ones, and with enhanced respect
                this process with strong opinions about what would work. All of us have had to
                pause, reflect, and sometimes change our minds as we studied these problems and
                citizens to study, reflect-and act.
            Thomas H. Kean, chair
            Lee H. Hamilton, vice chair
        
```

In examples 3 and 4, we see all the lines in the respective text files wherein the strings(given as arguments in the input command) did *not* appear. This command can be especially useful in filtering out unwanted or irrelevant lines from a text files and logs, perhaps making it easier to read and quicker to find desired information. In fact, a further application of this would be to store the outputs of this command into a new file each time and repeatedly filter out lines containing certain phrases until we find information pertaining to what we want.

### Source:
[16 grep Command Examples to Help You in Real-World - geekflare.com](https://geekflare.com/grep-command-examples/)

## Command Line Option 3: Match only Whole Words
The `$grep -w [pattern] [file]` file command finds and outputs lines only where the `[pattern]` occurs as a whole word, rather than including being a part of a larger word. For example, using the `-w` option with `"a"` would find all line occurences of `"a"`as the word itself, excluding words that simply have "a" inside them.

### Example 5:
Input command: `grep -w a 911report/preface.txt `

Output: `Democrats chosen by elected leaders from our nation's capital at a time of great

            We have come together with a unity of purpose because our nation demands it.
            
                September 11, 2001, was a day of unprecedented shock and suffering in the history of
                
                sharing information across a large and unwieldy government that had been built in a
                
                together as a nation. The test before us is to sustain that unity of purpose and
                
                meet the challenges now confronting us. We need to design a balanced strategy for
                
                have searched records and produced a multitude of documents for us. We thank
                
                assistance. We owe a huge debt to their investigative labors, painstaking attention
                
                This final report is only a summary of what we have done, citing only a fraction of
                
                inevitably will come to light. We present this report as a foundation for a better
                
                understanding of a landmark in the history of our nation.
                
            We also approach the task of recommendations with humility. We have made a limited`
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

### Source:
[grep Command in Linux with Examples (Search for a pattern in a file) - Reddit(r/commandline)](https://www.reddit.com/r/commandline/comments/m14s0y/grep_command_in_linux_with_examples_search_for_a/)



