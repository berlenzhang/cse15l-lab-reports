## Lab Report 3

# Part 1

**Failure inducing input:**

![Image](junitTest.jpg)

**Passing input:**

![Image](passingTest.jpg)

**Symptom:**

![Image](reversedTest.jpg)

**Before Code**

![Image](beforeCode.jpg)

**After Code**

![Image](afterCode.jpg)

The reason for the code failing was it was taking the values of `newArray` and inserting it into `arr`. `newArray` is an array full of zeros. The change fixed this issue by taking values from the input array `arr` and putting them into an empty array `newArray`. 

# Part 2

**`-m` Command**

Command input 1: `less -m technical/911report/chapter-12.txt`

Command output 1:

```
ATTACK TERRORISTS AND THEIR ORGANIZATIONS
            The U.S.government, joined by other governments around the world, is working through
                intelligence, law enforcement, military, financial, and diplomatic channels to
                identify, disrupt, capture, or kill individual terrorists. This effort was going on
                before 9/11 and it continues on a vastly enlarged scale. But to catch terrorists, a
                U.S. or foreign agency needs to be able to find and reach them.
            No Sanctuaries
            The 9/11 attack was a complex international operation, the product of years of
                planning. Bombings like those in Bali in 2003 or Madrid in 2004, while able to take
12%
```

Command input 2: `less -m technical/plos/journal.pbio.0020001.txt`

Command output 2:

```
 A Long Road Yet to Travel
        The positive trends in scientific productivity in Latin America should not be
        misinterpreted as a reason to be unconcerned about the existing gap highlighted by Mr.
        Annan. There are many compelling reasons for the push to increase scientific input from the
        developing world (Goldemberg 1998; Annan 2003). One is that science, as a discipline, would
        benefit from the contributions of many disparate groups around the world, rather than being
        dominated by two geographic regions. Many scientific problems could be solved much more
87%
```

**`G` Command**

Command input 1: pressing G after running `less technical/911report/chapter-1.txt`

Command output 1: 

```
The details of what happened on the morning of September 11 are complex, but they play out a simple theme. NORAD and the FAA were unprepared for the type of attacks launched against the United States on September 11, 2001. They struggled, under difficult circumstances, to improvise a homeland defense against an unprecedented challenge they had never before encountered and had never trained to meet.

    At 10:02 that morning, an assistant to the mission crew commander at NORAD's Northeast Air Defense Sector in Rome, New York, was working with his colleagues on the floor of the command center. In a brief moment of reflection, he was recorded remarking that "This is a new type of war."

    He was, and is, right. But the conflict did not begin on 9/11. It had been publicly declared years earlier, most notably in a declaration faxed early in 1998 to an Arabic-language newspaper in London. Few Americans had noticed it. The fax had been sent from thousands of miles away by the followers of a Saudi exile gathered in one of the most remote and impoverished countries on earth.

                
        
(END)
```

Command input 2: pressing G after running `less technical/plos/journal.pbio.0020001.txt`

Command output 2: 

```
Although the evidence presented here demonstrates that there is a long way to go before
        developing countries contribute a more equitable share to the international scientific
        community, there are also reasons to be optimistic. The relative increase in the number of
        publications, especially when corrected for the amount of money available in research and
        development, demonstrates that many developing countries are heading in the right
        direction. The extremely high scientific productivity of many developing nations, corrected
        for and despite the rather limited availability of funds, suggests that increased funding
        to the sciences will be an excellent investment by developing nations in terms of
        publications as a measure of scientific output, particularly if these publications can
        target the journals that have the greatest impact. Although there may still be a long road
        to travel, we feel optimistic that the bridges mentioned by Mr. Annan are slowly being
        built.
      
    
  
~
~
~
~
~
~
~
~
~
~
(END)
```

The source for this command is https://phoenixnap.com/kb/less-command-in-linux. This command is used to skip to the end of a file after you run `less`. This command can be useful when you are dealing with long files and you do not want to have to scroll down to the end of it.

**`less -N` Command**

Command input 1: `less -N technical/911report/chapter-12.txt`

Command output 1: 

```
1 
      2     
      3         
      4             WHAT TO DO? A GLOBAL STRATEGY
      5             REFLECTING ON A GENERATIONAL CHALLENGE
      6             Three years after 9/11, Americans are still thinking and talking about how to protect
      7                 our nation in this new era. The national debate continues. Countering terrorism has
      8                 become, beyond any doubt, the top national security priority for the United States.
      9                 This shift has occurred with the full support of the Congress, both major political
     10                 parties, the media, and the American people.
```

Command input 2: `less -N technical/plos/journal.pbio.0020001.txt`

Command output 2: 

```
1 
      2   
      3     
      4       
      5         
      6         Kofi Annan, the Secretary-General of the United Nations, recently called attention to
      7         the clear inequalities in science between developing and developed countries and to the
      8         challenges of building bridges across these gaps that should bring the United Nations and
      9         the world scientific community closer to each other (Annan 2003). Mr. Annan stressed the
     10         importance of reducing the inequalities in science between developed and developing
```

The source for this command is https://linuxize.com/post/less-command-in-linux/. This command numbers the lines of the file. This can be useful when you want to find a certain line or when you want to cite a part of the file. 

**& Command**

Command input 1: `less technical/911report/chapter-12.txt` `&American`

Command output 1:

```
Three years after 9/11, Americans are still thinking and talking about how to protect
                parties, the media, and the American people.
            This pattern has occurred before in American history. The United States faces a
                through the processes of the American republic.
                consider what to do-the shape and objectives of a strategy. Americans should also
                has taught us that terrorism against American interests "over there" should be
                regarded just as we regard terrorism against America "over here." In this same
                sense, the American homeland is the planet. But the enemy is not just "terrorism,"
                mean exactly what they say: to them America is the font of all evil, the "head of
```

Command input 2: `less technical/plos/journal.pbio.0020001.txt` `&trend`

Command output 2:

```
implied? A closer look at the trends over the last decade reveals important advances in
        Canada and United States, the trend in Latin America has been an increase in relative
        the decreasing trends in the number of publications per investment dollar in Canada and
        United States could reflect a trend towards more costly research in larger scientific
        The positive trends in scientific productivity in Latin America should not be
```

The source for this command is https://man7.org/linux/man-pages/man1/less.1.html. This command searches for the input that comes after the `&`. For example, if you run the command `&hello` you will skip to the nearest instance of the word 'hello'. This command would be useful if you wanted to look for a specific part of the file.


