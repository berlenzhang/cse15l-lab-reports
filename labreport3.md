# Bugs

**Failure Inducing Input:**

```
@Test
  public void testReverse2() {
    int[] input2 = {1, 2, 3};
    assertArrayEquals(new int[]{3, 2, 1}, ArrayExamples.reversed(input2));
  }
```

**Successful Input:**

```
@Test
  public void testReversed() {
    int[] input1 = { };
    assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
  }
```

**Symptom:**

![Image](SymptomsScreenshot.jpg)

**Before**

```
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
```

**After**

```
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      newArray[i] = arr[arr.length - i - 1)];
    }
    return newArray;
  }
```

The issue with the code shown in the before image was that it was taking values from the `newArray` and using them to replace elements in `arr`. Since `newArray` is an empty array, the code would just replace all the values of the given array with zeros. The after code fixed this issue by taking the values from the first array and inserting them into the empty `newArray` backwards. Then, `newArray` is returned.


# Researching Commands

**`less -N` Command From Source https://www.geeksforgeeks.org/less-command-linux-examples/**

Input 1: `less -N technical/911report/chapter1.txt`

Output 1:

```
1 
      2         
      3                 
      4 "WE HAVE SOME PLANES"
      5 
      6     Tuesday, September 11, 2001, dawned temperate and nearly cloudless in the eastern 
      6 United States. Millions of men and women readied themselves for work. Some made their 
      6 way to the Twin Towers, the signature structures of the World Trade Center complex in 
      6 New York City. Others went to Arlington, Virginia, to the Pentagon. Across the Potomac
      6  River, the United States Congress was back in session. At the other end of Pennsylvan
      6 ia Avenue, people began to line up for a White House tour. In Sarasota, Florida, Presi
      6 dent George W. Bush went for an early morning run.
      7 
      8     For those heading to an airport, weather conditions could not have been better for
      8  a safe and pleasant journey. Among the travelers were Mohamed Atta and Abdul Aziz al 
      8 Omari, who arrived at the airport in Portland, Maine.
```

Input 2: `less -N technical/biomed/1468-6708-3-4.txt`

Output 2: 
```
1 
      2   
      3     
      4       
      5         Introduction
      6         With the exception of counting deaths from all causes
      6 , a
      7         common problem in clinical trials is the missing data
      8         caused by patients who do not complete the study in f
      8 ull
      9         schedule and drop out of the study without further
     10         measurements. Possible reasons for patients dropping 
     10 out of
```

This command shows the text numbered lines. This can be useful for finding a specific line.

**`less -m` Command From Source https://man7.org/linux/man-pages/man1/less.1.html**

Input 1: `less -m technical/911report/chapter2.txt`

Output 1: 
```
 THE FOUNDATION OF THE NEW TERRORISM
            A DECLARATION OF WAR
            In February 1998, the 40-year-old Saudi exile Usama Bin Ladin and a f
ugitive Egyptian
                physician, Ayman al Zawahiri, arranged from their Afghan headquar
ters for an Arabic
                newspaper in London to publish what they termed a fatwa issued in
 the name of a
                "World Islamic Front." A fatwa is normally an interpretation of I
slamic law by a
                respected Islamic authority, but neither Bin Ladin, Zawahiri, nor
 the three others
                who signed this statement were scholars of Islamic law. Claiming 
that America had
                declared war against God and his messenger, they called for the m
urder of any
                American, anywhere on earth, as the "individual duty for every Mu
slim who can do it
                in any country in which it is possible to do it."
            
            Three months later, when interviewed in Afghanistan by ABC-TV, Bin La
din enlarged on
                these themes.
            
            He claimed it was more important for Muslims to kill Americans than t
o kill other
                infidels." It is far better for anyone to kill a single American 
soldier than to
                squander his efforts on other activities," he said. Asked whether
 he approved of
2%
```

Input 2: `less -m technical/government/Env_Prot_Agen/bill.txt`

Output 2: 
```
(1)
The term "actual 1985 emission rate", for electric
utility units means the annual sulfurdioxide or nitrogen oxides
emission rate in pounds per million Btu as reported in the NAPAP
Emissions Inventory, Version 2, National Utility Reference File.
For nonutility units, the term "actual 1985 emission rate" means
the annual sulfur dioxide or nitrogen oxides emission rate in
pounds per million Btu as reported in the NAPAP Emission Inventory,
Version 2.


(2)
The term "allowable 1985 emissions rate" means a
federally enforceable emissionslimitation for sulfur dioxide or
oxides of nitrogen, applicable to the unit in 1985 or the
limitation applicable in such other subsequent year as determined
by the Administrator if such a limitation for 1985 does not exist.
Where the emissions limitation for a unit is not expressed in
pounds of emissions per million Btu, or the averaging period of
that emissions limitation is not expressed on an annual basis, the
Administrator shall calculate the annual equivalent of that
emissions
29%
```

This command displays a percentage that indicated how far you are in the text of the file. This can be useful to figure out what part of the file you are currently looking at.


**`&` Command From Source https://phoenixnap.com/kb/less-command-in-linux**

Input 1: `less technical/911report/chapter-9.txt` then `&September`

Output 1: 
```
Emergency response is a product of preparedness. On the morning of September 11,
                Some civilians have told us that their evacuation on September 11 was greatly aided
            Six weeks before the September 11 attacks, control of the WTC was transferred by net
                were no longer part of the official chain of command. However, on September 11, most
                the WTC on September 11, the WTC fire safety plan remained essentially the
            Port Authority Police Department. On September 11, 2001, the Port Authority of New
            As of September 11, the Port Authority lacked any standard operating procedures to
            As of September 11, FDNY companies and chiefs responding to a fire used analog,
                of September 11, they were not prepared to comprehensively coordinate their efforts
            As we turn to the events of September 11, we are mindful of the unfair perspective
```

Input 2: `less technical/biomed/1471-213X-3-7.txt` then `&animals`

Output 2: 
```
 Many animals have evolved to survive seasonally
        In most animals diapause can occur only at a specific
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
~
~
~
```

This command finds lines that contain the inputed word. This can be useful if you want to find a specific word in the file.

**`G` Command From Source https://linux.die.net/man/1/less**

Input 1: `less technical/biomed/1471-230X-1-10.txt` then `G`

Output 1: 
```
 Competing Interests
        None declared.
      
      
        Grant Support
        Part of this work was supported by a VA Merit Review
        Grant
      
      
        Abbreviations
        IBAT: ileal bile acid transporter; CFTR: cystic fibrosis
        transmembrane conductance regulator. This is the protein
        product of the Cystic Fibrosis gene and is considered to
        act as a Cl channel. TBS: Tris-buffered saline.
      
    
  
(END)
```

Input 2: `less technical/911report/chapter-5.txt` then `G`

Output 2: 
```
                   and give them necessary training;
                an intelligence effort to gather required information and form assessments of
                    enemy strengths and weaknesses;
                the ability to move people; and
                the ability to raise and move the necessary money.
            
            The information we have presented about the development of the planes operation shows
                how, by the spring and summer of 2000, al Qaeda was able to meet these requirements.
            By late May 2000, two operatives assigned to the planes operation were already in the
                United States. Three of the four Hamburg cell members would soon arrive.
        
    
(END)
```

This command jumps to the end of the file. This can be helpful if you want to skip to the end of a file.

