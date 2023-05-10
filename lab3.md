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
Input command: `grep -w a 911report/preface.txt`

Output: 
```Democrats chosen by elected leaders from our nation's capital at a time of great
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
   We also approach the task of recommendations with humility. We have made a limited
```

### Example 6:
Input command: `grep -w in plos/journal.pbio.0020064.txt` 

Output: 
```
        poison could result in near-instant expiration. And now, as researchers begin to understand
        on the tongue and elsewhere in the mouth (Figure 1). Up to 100 taste receptor
        cells—epithelial cells with some neuronal properties—are arranged in each taste bud. In the
        Taste is the sense by which the chemical qualities of food in the mouth are
        ‘basic taste’, explains Bernd Lindemann, now retired but an active taste researcher in
        explains Lindemann: ‘Food is already in the mouth. We just have to decide whether to
        sense system. Then, in 1991, the first olfactory receptors were described. These proteins,
        which are exposed on the surface of cells in the nose, bind to volatile chemicals and allow
        us to detect smells. This landmark discovery, in part, encouraged many established taste
        explains Zuker, who previously worked on other sensory systems in flies, ‘there was a
        disconnect between our understanding of sensations in the case of photoreception,
        involved in sweet and bitter taste, ‘but the receptors weren't known, so we started to look
        variation might be due to alterations in the coding sequence for a bitter receptor, the
        All these receptors, says Zuker, are coexpressed in bitter taste receptor cells, a
        receptors would be expressed in each bitter taste cell. We just need to know if something
        The sweet receptor story started in 1999 with the identification of two putative
        researchers at the University of Miami (Florida, United States) School of Medicine in 2000.
        T1R3. In October 2003, Zuker and his coworkers reported that mice in which either T1R1 or
        tastant. However, other researchers reported in August 2003 that T1R3 knockouts retain some
        not alone, however, in thinking there may be more than one umami receptor (and additional
        The salty and sour receptors may be very different from the GPCRs involved in bitter,
        channel through which specific inorganic ions can diffuse. Changes in cellular ion
        States) says there are at least two ion channel receptors for salt in rodent taste receptor
        channel only responds to sodium chloride—and may be the more important receptor in
        Sour tastants are acids, often found in spoiled or unripe food. DeSimone's current idea
        identified the proton channel involved in sour taste as well as an ion channel that could
        channels are essential elsewhere in the body, as DeSimone suspects, to avoid lethality he
        will need to construct conditional knockouts in which the channel is lost only in the taste
        sour perception are correct. And, he says, GPCRs could also be involved in these
        question in taste perception: how is taste coded? When we eat, our tongue is bombarded with
        umami fits the labelled-line model in the periphery of the taste system. Their expression
        data show that receptors for these qualities are expressed in distinct populations of taste
        cells. In addition, in early 2003, they reported that, as in other sensory systems, a
        sweet, or umami, and engineered them so that PLCβ2 was only expressed in bitter
        colleagues described mice in which a non-taste receptor—a modified κ-opioid receptor that
        can only be activated by a synthetic ligand—was expressed only in cells expressing T1R2,
        example, believe that there is at least some involvement of cross-fibre patterning even in
        labelled line for bitter, sweet, and umami’. Bartoshuk also says the debate is decided in
        favour of the labelled-line model in the periphery. The crossfibre model is an interesting
        seen. However, it seems certain that, as in the past five years, the next five years will
        see large advances in our knowledge of many aspects of taste, a fascinating and important
        relatively little is known about the transduction pathways in taste, how taste cells talk
        to the nervous system, or about events further downstream in the brain. How are signals
        tell us not only about taste but about how the nervous system in general is put together,
        blood pressure. Lindemann also sees a great future in artificial ligands for taste
        receptors. The sense of taste is partly lost in elderly people, he says, so better
```

In examples 5 and 6, we see that this command outputs all lines in the text file that *only* contain the entire word that was specified as an argument. This command can be useful in situations where you want to look for occurences of a word by its *meaning* rather than its face-value string value. Let's say you wanted to search for lines with the word "ore". There could be other words which contain the string "ore" inside, but that is not at all related to what we wanted. With `-w`, we can filter out unwanted partial matches.

### Sources:
[grep Command in Linux with Examples (Search for a pattern in a file) - Reddit(r/commandline)](https://www.reddit.com/r/commandline/comments/m14s0y/grep_command_in_linux_with_examples_search_for_a/)

[16 grep Command Examples to Help You in Real-World - geekflare.com](https://geekflare.com/grep-command-examples/)

## Command Line Option 4: Ignore case distinctions
The `$ grep -i [pattern] [file]` command finds and outputs all the lines that contain the string specified by `[pattern]`, except it ignores all upper and lower cases. Any line with the instance of that string in any combination of upper and/or lower cases will be outputed.
### Example 7:
Input command: `grep -i we 911report/preface.txt`

Output: 
```
            We present the narrative of this report and the recommendations that flow from it to
            We have come together with a unity of purpose because our nation demands it.
                the United States. The nation was unprepared. How did this happen, and how can we
            To answer these questions, the Congress and the President created the National
            Our mandate was sweeping. The law directed us to investigate "facts and circumstances
                areas determined relevant by the Commission. In pursuing our mandate, we have
                reviewed more than 2.5 million pages of documents and interviewed more than 1,200
                our mandate. We have sought to be independent, impartial, thorough, and nonpartisan.
                From the outset, we have been committed to share as much of our investigation as we
                can with the American people. To that end, we held 19 days of hearings and took
            We learned about an enemy who is sophisticated, patient, disciplined, and lethal. The
                and equal rights for women. It makes no distinction between military and civilian
            We learned that the institutions charged with protecting our borders, civil aviation,
                adjust their policies, plans, and practices to deter or defeat it. We learned of
                fault lines within our government-between foreign and domestic intelligence, and
                between and within agencies. We learned of the pervasive problems of managing and
            At the outset of our work, we said we were looking backward in order to look forward.
                We hope that the terrible losses chronicled in this report can create something
                positive-an America that is safer, stronger, and wiser. That September day, we came
                meet the challenges now confronting us. We need to design a balanced strategy for
                the long haul, to attack terrorists and prevent their ranks from swelling while at
                the same time protecting our country against future attacks. We have been forced to
                agencies that prevailed in the great struggles of the twentieth century must work
                together in new ways, so that all the instruments of national power can be combined.
                Congress needs dramatic change as well to strengthen oversight and focus
            As we complete our final report, we want to begin by thanking our fellow
                Commissioners, whose dedication to this task has been profound. We have reasoned
                dialogue. We want to express our considerable respect for the intellect and judgment
                of our colleagues, as well as our great affection for them.
            We want to thank the Commission staff. The dedicated professional staff, headed by
                have been superb. We thank the Congress and the President. Executive branch agencies
                have searched records and produced a multitude of documents for us. We thank
                officials, past and present, who were generous with their time and provided us with
                assistance. We owe a huge debt to their investigative labors, painstaking attention
                to detail, and readiness to share what they have learned. We have built on the work
                of several previous Commissions, and we thank the Congressional Joint Inquiry, whose
                fine work helped us get started. We thank the City of New York for assistance with
            We conclude this list of thanks by coming full circle: We thank the families of 9/11,
                the importance of the work we have undertaken.
            We want to note what we have done, and not done. We have endeavored to provide the
                most complete account we can of the events of September 11, what happened and why.
                This final report is only a summary of what we have done, citing only a fraction of
                the sources we have consulted. But in an event of this scale, touching so many
                issues and organizations, we are conscious of our limits. We have not interviewed
                inevitably will come to light. We present this report as a foundation for a better
            We have listened to scores of overwhelming personal tragedies and astounding acts of
                heroism and bravery. We have examined the staggering impact of the events of 9/11 on
                the American people and their amazing resilience and courage as they fought back. We
                preparing to respond if it becomes necessary. We emerge from this investigation with
                for the American people. We recognize the formidable challenges that lie ahead.
            We also approach the task of recommendations with humility. We have made a limited
                number of them. We decided consciously to focus on recommendations we believe to be
                most important, whose implementation can make the greatest difference. We came into
                pause, reflect, and sometimes change our minds as we studied these problems and
                considered the views of others. We hope our report will encourage our fellow
```
### Example 8:
From the reddit link attatched below in the sources section, I found that I could combine this `-i` command with one we previously learned (`-w`) to find all lines with a specific *whole word, ignoring cases.* We can do this with the `-wi` command.

Input command: `grep -wi as 911report/chapter-11.txt` 

Output: 
```
            As time passes, more documents become available, and the bare facts of what happened
                reimagine, as that past world, with its preoccupations and uncertainty, recedes and
                in Korea another. But these were attacks by major powers. While by no means as
                threatening as Japan's act of war, the 9/11 attack was in some ways more
                satisfaction. The people of the United States hoped to enjoy a peace dividend, as
            The United States emerged into the post-Cold War world as the globe's preeminent
                Kosovo. America stood out as an object for admiration, envy, and blame. This created
                Kansi, who in 1993 killed two CIA employees as they waited to go to work in Langley,
            As best we can determine, neither in 2000 nor in the first eight months of 2001 did
                as Serbian ethnic cleansing, biological attacks, Iraqi weapons of mass destruction,
                increase over the next several years. It specified as particular points of
                vulnerability the White House, the Capitol, symbols of capitalism such as Wall
                Street, critical infrastructure such as power grids, areas where people congregate
                such as sports arenas, and civil aviation generally. It warned that the 1993 World
            This 1995 estimate described the greatest danger as "transient groupings of
                sentence:"Iran and its surrogates, as well as terrorist financier Usama Bin Ladin
                the highest officials in the government with titles such as "Bin Ladin Threatening
                about ten analysts to this effort was seen as a major bureaucratic victory, but the
                discounted the alarms about a catastrophic threat as relating only to the danger of
                months before 9/11:"It would be a mistake to redefine counterterrorism as a task of
            Therefore, those government experts who saw Bin Ladin as an unprecedented new danger
                Intelligence Estimate is noticed in the Congress, for example. But, as we have said,
            By 2001 the government still needed a decision at the highest level as to whether al
                al Qaeda as the "point of the spear of radical Islam." But no one forced the
                the threat. The issue was never joined as a collective debate by the U.S.
            Institutionalizing Imagination: The Case of Aircraft as Weapons
                to Japanese examination of Hawaii as a possible target. But, another historian
                imagine that aircraft could be used as weapons. Indeed, since al Qaeda and other
                other vehicles such as boats (the Cole attack) or planes is not far-fetched. Yet
                experts. In 1996, as a result of the TWA Flight 800 crash, President Clinton created
                hijackings or the use of aircraft as weapons. It focused mainly on the danger of
                such as the "Blind Sheikh," Omar Abdel Rahman. Had the contents of this PDB been
            The North American Aerospace Defense Command imagined the possible use of aircraft as
                put aside in the early planning of the exercise as too much of a distraction from
                the main focus (war in Korea), and as too unrealistic. As we pointed out in chapter
                used as a weapon. It did not perform this kind of analysis from the enemy's
                warning system was not looking for information such as the July 2001 FBI report of
                enemy that, as the twentieth century closed, was most likely to launch a surprise
                with the threat was to end al Qaeda's ability to use Afghanistan as a sanctuary for
                proxies to try to capture or kill Bin Ladin and his lieutenants. As early as
                of Afghanistan as practically inconceivable before 9/11. It was never the subject of
                repeatedly did not make it more effective. As evidence of al Qaeda's responsibility
                region, prepared to fire cruise missiles. General Hugh Shelton developed as many as
            As for the Department of Defense, some officers in the Joint Staff were keen to help.
                2000, as part of a millennium after-action review. President Clinton and his
                accepting what are viewed as givens, including that efforts to identify and fix
                medications. What is missing is the attending physician who makes sure they work as
                NSA did not think its job was to research these identities. It saw itself as an
                agency to support intelligence consumers, such as CIA. The NSA tried to respond
                almost the same day as the one given to Khalid al Mihdhar.
                identify one of the travelers as Khalid al Mihdhar. After the flight left, they
            The information arrived at Bangkok too late to track these travelers as they came in.
                Had the authorities there already been keeping an eye out for Khalid al Mihdhar as
                challenge of managing a transnational case, one that hopped from place to place as
                organizations as disparate as the CIA, the FBI, the State Department, the military,
                strategy for a war on terrorism. It was to rebuild the CIA. They said the CIA as a
            As some officials pointed out to us, there is a tradeoff in this management approach.
                security community. As a consequence, one of the critical working relationships in
                period in which the government as a whole seemed to be acting in concert to deal
```

In example 7, we see all lines in the `911report/preface.txt` file that had contained the `"we"` string in any combination of lower and upper cases. In example 8, we see all lines in the `911report/chapter-11.txt`` file that had contained the `"as"` *word* in any combination of lower and upper cases.

### Sources:
[grep Command in Linux with Examples (Search for a pattern in a file) - Reddit(r/commandline)]
(https://www.reddit.com/r/commandline/comments/m14s0y/grep_command_in_linux_with_examples_search_for_a/)

[16 grep Command Examples to Help You in Real-World - geekflare.com](https://geekflare.com/grep-command-examples/)


