## Lab Report 3
---
# Researching Commands
For this lab, I have chosen the command `grep`. `grep` is short for **“global regular expression print”** and it is a command that searches for a pattern within a file and it displays it out. This command is important because grep allows you to search for a pattern quickly and efficiently in many ways. Instead of just counting a particular word or searching through every file, `grep` will do all of that in a timely manner. 

---
# First command
- This searches for the string recursively in all files in the current directory. `grep -r` is important because it allows you to search for a pattern in all files instead of just searching through every file. For instance if you have around 1000 files, you would not want to go through each individual file as that will take too much time. You can just use `grep -r` to search through every file for a particular pattern. 

**First Example**
- In this example it searches for the word "revolutionizing" recursively in the current directory technical.

```
julieli@Julies-MacBook-Pro technical % grep -r "revolutionizing"
./plos/pmed.0010058.txt:        New immunomodulatory agents offer the greatest hope of revolutionizing the field. New drug
./biomed/1472-6750-3-11.txt:        an important role in revolutionizing research in the field
./biomed/gb-2003-4-4-r28.txt:        revolutionizing biology. That much is universally agreed.
```

**Second Example**
- In this example it searched for the word "consortia" recursively in the current directory technical.

```
julieli@Julies-MacBook-Pro technical % grep -r "consortia"
./government/Media/Terrorist_Attack.txt:City Bar and by emergency consortia of large Manhattan firms to
./plos/pmed.0020210.txt:        backed new initiatives. There are also a number of new academic consortia with novel
./plos/pmed.0020210.txt:        academic–industrial collaborations supporting preclinical development in consortia like
./plos/pmed.0020210.txt:        beyond research traditionally thought of as academic. New consortia modeled after the three
./plos/journal.pbio.0020010.txt:        financial planning had in coming to terms with consortial purchases delayed its growth as
./plos/journal.pbio.0020010.txt:        an access service. Although selling to consortia of academic libraries may not have
./plos/journal.pbio.0020010.txt:        improved JSTOR's financial position in the short-term, consortia are a route to spreading
./plos/journal.pbio.0020010.txt:        individual institutions rather than from consortia. I sympathise with Roger Schonfeld in
```
---
# Second command
- For this second command `grep -r -l` searches for the pattern recursively in all files under the directory ./technical and displays only the filenames. This is important when you want to search for the same pattern in all files, but you only want to only see the file names. You can take just the file names for other commands and it makes looking at the data more easier to see.

**First Example**
- In this example it searches for the word "consortia" recursively in all files, but only displays 4 file names.

```
julieli@Julies-MacBook-Pro technical % grep -r -l "consortia"  
./government/Media/Terrorist_Attack.txt
./plos/pmed.0020210.txt
./plos/journal.pbio.0020010.txt
```
**Second Example**
- In this example it searches for the word "revolutionizing" recursively in all files, but only displays 4 file names.

```
julieli@Julies-MacBook-Pro technical % grep -r -l "revolutionizing"
./plos/pmed.0010058.txt
./biomed/1472-6750-3-11.txt
./biomed/gb-2003-4-4-r28.txt
```
---
# Third command
- For this third command it counts the number of lines that contain the word in the file. This is important to use when you want to see how many times a word is used in a single file. For instance if you have a huge text file with a lot of paragraphs and you don't want to individually count each word because that would take too long, you use `grep -c "word" <file>` to count that word. 

**First Example**
-In this example it counts how many times "consortia" shows up in the file ./plos/pmed.0020210.txt which is 3 times.

```
julieli@Julies-MacBook-Pro technical % grep -c "consortia" ./plos/pmed.0020210.txt 
3
```
**Second Example**
-In this example it counts how many times "revolutionizing" shows up in the file ./plos/pmed.0010058.txt which is 1 time.

```
julieli@Julies-MacBook-Pro technical % grep -c "revolutionizing" ./plos/pmed.0010058.txt 
1
```
---
# Fourth command
- For the fourth command it searches for lines that do not contain the word in the single file. This is useful because when you want to search for sentences or paragraphs that do not contain that word, then you can use that command to do it immediately. For instance, you do not want a particular word because it is not the same topic from what you are trying to read so you can weed it out by using `grep -v "word" <file>`. 

**First Example**
- In this example it displays all the text that does not contain the word "of" within the file ./biomed/1471-2490-3-2.txt.

```
julieli@Julies-MacBook-Pro technical % grep -v "of" ./biomed/1471-2490-3-2.txt

  
    
      
        Background
        urology and uro-radiology. The technology allows the rapid
        2 3 4 5 ] . Its sensitivity and specificity is reported to
        be more than 95% and 96 % respectively [ 1 2 3 4 5 6 ] . An
        important disadvantage is a higher radiation dose to the
        versus 4.7 mSv in the radiation dose to the patient between
        IVU and UHCT performed for renal colic.
        accuracy, and its ability to suggest an alternative
        is valuable in diagnosing many significant diseases earlier
        in their course, which may be helpful in decreasing the
        associated morbidity. In this study, we are presenting our
        flank pain.
      
      
        Methods
        The radiologist's reports on CT, CT films and medical
        2000 and August 2001 at a University Hospital for suspected
        renal/ureteral colic were reviewed. The UHCT were obtained
        on a Cti/pro single slice helical CT scanner (General
        Electrical medical systems, Milwaukee, WI). The exposure
        factors setting were KVp 130 and mAS 200-250. All scans
        contrast material. Patients were placed in supine position
        Additional prone films were taken whenever the radiologist
        otherwise suspected were analyzed. All relevant
        radiological, biochemical, serological investigations as
        well as per-operative findings were also analyzed.
      
      
        Results
        From July 19, 2000 to August 15, 2001, 233 patients had
        calculi were identified in 148 examinations (64%), findings
        patients were lost to follow up and therefore were not
        included. In the remaining 201 patients, sensitivity and
        respectively while +ve and -ve predictive value was 99% and
        98% respectively. Twenty-eight patients (12%) had
        alternative or additional diseases (other than renal,
        ureteric or bladder stone disease) diagnosed on UHCT.
        Table 1describes in detail the alternative or additional
        diagnoses.
        surgical procedure, biopsy and biochemical evaluation (in
      
      
        Discussion
        diagnoses can be identified on UHCT performed for suspected
        ureteral/renal colic [ 9 10 11 12 13 ] . Apart from its
        high sensitivity and specificity for diagnosing stone
        from other modalities, is its ability to pick up other
        unsuspected significant clinical entities. Early diagnosis
        pancreatitis, diverticulitis and leaking aortic aneurysm
        that require urgent and prompt treatment could affect the
        associated morbidity and mortality associated with such
        renal/ureteric colic, Katz [ 13 ] reported 101 patients
        (10%) with alternative or incidental diagnosis.
        on this subject.
        Among the major series published on the subject [ 9 10
        was 10-15%. The disease pattern is remarkably similar in
        most series (Table 2). In one report from Albert Einstein
        Medical Center, Philadelphia, Marcella et al [ 8 ] noted an
        our series by comparison to other series. It is important
        should be taken to rule out alternative diagnosis for flank
        pain.
        cholecystitis, mesenteric lymphadenitis, pyelonephritis and
        appendicitis, initiated early treatment. The alternative
        in other series is interesting. It suggests that UHCT may
        change the prognosis in many cases that would otherwise be
        diagnosed late.
      
      
        Conclusion
        diagnoses can be reliably identified on UHCT performed for
        suspected renal/ureteric colic. In the present series, such
        diverticulitis.
      
      
        Competing interests
        None declared.
      
      
        Authors' contribution
        NAA collected data and participated in manuscript
        writing
        and participated in writing the manuscript.
        and participated in writing the manuscript.
        All authors read and approved the final manuscript.
  ```

**Second Example**
- In this example it displays all the text that does not contain the word "JSTOR" within the file ./plos/journal.pbio.0020010.txt.

```
julieli@Julies-MacBook-Pro technical % grep -v "JSTOR" ./plos/journal.pbio.0020010.txt

  
    
      
        
        vision was of a solution to libraries' ever-voracious demands for space to house paper
        volumes. The idea was that libraries could save space by removing volumes available in
        libraries without the paper volumes have been able to offer their users access to the
        but electronic holdings have increased. So a space-saving service became an access
        service.
        decision to use page images may have been eight years ago, future user-friendly access
        requires searching capabilities across full-text, which page images cannot supply.
        Likewise, the decision to digitise the back-runs of around 100—now 218—paper journals was a
        bold decision at the time, but the future for access to journal literature lies in
        electronic versions of thousands rather than hundreds of titles, both current and
        hundred titles. Its technical solutions and financial models look dated as both
        subscription-based and open-access publishers improve their services to authors and to
        will be seen as a small-scale pioneer from which we learned valuable lessons.
        Learned’, many of which are relevant to current access initiatives. The need for grant
        funding to launch any such initiative has to be accompanied by a sound business plan to
        Kevin Guthrie, who found the quickest way through the maze of conflicting advice—much of
        publishing communities to buy into a product that was only a promise. Meeting user needs
        for easy access to high-quality content was the key to the fulfilment of that promise.
        to become the hallmark of the new open-access initiatives as they develop.
        financial planning had in coming to terms with consortial purchases delayed its growth as
        an access service. Although selling to consortia of academic libraries may not have
        access and therefore securing longer-term financial stability (as the major publishers have
        realised through their ‘Big Deals’ in selling hundreds of journals to hundreds of libraries
        in a consortium). Some opportunities were also delayed—not lost—through too slow an
        Kingdom being the exception. The UK deal was with JISC, the Joint Information Systems
        Committee of the UK Higher Education Funding Councils, acting more as a negotiating agent
        than a consortium, and this model could have been applied in other countries. More
        to be imaginative. For all vendors, there has to be an understanding of the political,
        social, economic, and educational structure of the country into which the product is being
        sold, an understanding that takes time to acquire but that pays dividends. Open-access
        publishers do not have to sell their product to users of their journals, but local
        knowledge is essential in ‘selling’ their services to authors. The globalisation of
        publishing has combined with the globalisation of the networks and with the globalisation
        of research to provide opportunities for high-quality research conducted outside North
        America and Western Europe to be published in peer-reviewed open-access journals more
        readily than in the traditional subscription-based journals.
        the history of electronic publication through a minute examination of the process leading
        its comprehensiveness cannot be questioned, but one small omission of which I have personal
        knowledge makes me question the value of so much detail. The omission concerns the interest
        considered. Not a detail of world-shattering significance, but it does illustrate the fact
        individual institutions rather than from consortia. I sympathise with Roger Schonfeld in
        attempting to write such a comprehensive history, but what is the point of appearing to be
        comprehensive when comprehensiveness is an impossible goal? Would a briefer history have
        been just as valuable?
        fascinating and instructive history of an important and ground-breaking initiative. Bill
        Bowen's vision may not have developed in quite the way he expected, but the ‘bottom-line’
        is that the vision did become a successful reality. The problem of ever-expanding libraries
        others to develop services that are more in accord with 2003 than 1993. One lesson Roger
        Schonfeld does not draw out is the pace of change in electronic publishing, and if so much
        has been achieved since 1993, what promise is held out by the next ten years'!
  ```
---
All commands and descriptions have been asked by ChatGpt.
> I asked ChatGpt to give me a list of grep commands and the importance of each one. 
> So it gave me 8 options to choose from
**Example 1**
> `grep -r "pattern" ./technical`
> I just changed the word twice to `"revolutionizing"` and `"consortia"` and since I already did `cd technical` I did not have to add that add `./technical` at the end of the command.
> I also grabbed the meaning they used for the command and changed it up a bit = *"The -r option enables recursive searching through directories, allowing grep to search for a pattern in files within subdirectories."*
**Example 2**
>For the 2nd example it gave me the same version but just changes it to `grep -r -l "pattern" ./technical` 
>I changed the word again and didnt add technical at the end.
>I also took their meaning of the command.
**Example 3**
> `grep -c "pattern" ./technical/file.txt`
> For this command I changed the word again and I added in my own file.
> I took their meaning of this command and changed it up = *"The -c option counts the number of lines that match the given pattern instead of displaying the matching lines."*
**Example 4**
> `grep -v "pattern" ./technical/file.txt`
> For this command I changed the word and put in a different file for both examples. 
> I also used their meaning of this command= *"The -v option inverts the match, displaying lines that do not match the given pattern."*


