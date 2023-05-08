## Lab Report 3
---
# Researching Commands
For this lab, I have chosen the command `grep`. `grep` is short for **“global regular expression print”** and it is a command that searches for a pattern within a file and it displays it out. 

---
# First command

First Example
-This searches for the string recursively in the current directory.

```
julieli@Julies-MacBook-Pro technical % grep -r "revolutionizing"
./plos/pmed.0010058.txt:        New immunomodulatory agents offer the greatest hope of revolutionizing the field. New drug
./biomed/1472-6750-3-11.txt:        an important role in revolutionizing research in the field
./biomed/gb-2003-4-4-r28.txt:        revolutionizing biology. That much is universally agreed.
```

Second Example

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

# Second command
-Search for the word "password" recursively in all files under the directory ./technical and display only the filenames.

First Example
```
julieli@Julies-MacBook-Pro technical % grep -r -l "consortia"  
./government/Media/Terrorist_Attack.txt
./plos/pmed.0020210.txt
./plos/journal.pbio.0020010.txt
```
Second Example
```
julieli@Julies-MacBook-Pro technical % grep -r -l "revolutionizing"
./plos/pmed.0010058.txt
./biomed/1472-6750-3-11.txt
./biomed/gb-2003-4-4-r28.txt
```

# Third command
- This option tells grep to perform a case-insensitive search. This is useful when you want to search for a pattern without being case-sensitive.

First Example

Second Example

# Fourth command
- This option tells grep to select non-matching lines. This is useful when you want to search for lines that do not contain a specific pattern.

First Example

Second Example


