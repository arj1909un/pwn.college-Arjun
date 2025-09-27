#1. Matching with *

Now, practice this yourself! Starting from your home directory, change your directory to `/challenge`, but use globbing to keep the argument you pass to `cd` to at most four characters! Once you're there, run `/challenge/run` for the flag!


**flag:** `pwn.college{sES1qpImQeSgFqqHme848knAMED.QXxIDO0wSM0EzNzEzW}`

Command used: 
`cd /ch*`
`/challenge/run`

I had to change my directory to `/challenge` but according to the condition I cannot use more than 4 characters. Therefore, I used the command `cd /ch*`, `*` matches everything after previously passed characters. 
After changing directories, I ran `/challenge/run` to obtain the flag. 


#2. Matching with ? 

Now, practice this yourself! Starting from your home directory, change your directory to `/challenge`, but use the `?` character instead of `c` and `l` in the argument to `cd`! Once you're there, run `/challenge/run` for the flag!

**flag:** `pwn.college{gslWQ17sg49MxAuNQJ9bONESSND.QXyIDO0wSM0EzNzEzW}`

Command used: 
`cd /?ha??enge`
`/challenge/run`

`?` is used to match the characters according to the passed argument. According to the challenge, I had to use `?` instead of `c` , `l`, therefore I did just that. I ran `/challenge/run` after that to get the flag. 


#3. Matching with []

Try it here! We've placed a bunch of files in `/challenge/files`. Change your working directory to `/challenge/files` and run `/challenge/run` with a single argument that bracket-globs into `file_b`, `file_a`, `file_s`, and `file_h`!

**flag:** `pwn.college{QTWkNOTyvElzIm4kE0NQo8yixkM.QXzIDO0wSM0EzNzEzW}`

Command used: 
`cd /challenge/files`
`/challenge/run file_[absh]`

I changed my directory to `/challenge/files` as per mentioned in the challenge. My job was to bracket-glob  and I did just that using the command `/challenge/run file_[bash]`. 

#### What I learnt: 
The square brackets are, essentially, a limited form of `?`, in that instead of matching any character, `[]` is a wildcard for some subset of potential characters, specified within the brackets. For example, `[pwn]` will match the character `p`, `w`, or `n`



#4. Matching paths with []

Now it's your turn. Once more, we've placed a bunch of files in `/challenge/files`. Starting from your home directory, run `/challenge/run` with a single argument that bracket-globs into the absolute paths to the `file_b`, `file_a`, `file_s`, and `file_h` files!

Command used: 
`/challenge/run /challenge/files/file_[bash]`

flag: `pwn.college{E7thTl6olJt_itJIqlVzzkw7nMA.QX0IDO0wSM0EzNzEzW}`

Essentially, what I learnt is that we can pass in absolute file paths for globbing with square brackets as well. 



#5. Multiple globs

Now you try it. We put a few happy, but diversely-named files in `/challenge/files`. Go `cd` there and run `/challenge/run`, providing a single argument: a short (3 characters or less) globbed word with two `*` globs in it that covers every word that contains the letter `p`.

**flag:** `pwn.college{gF_LhT43Fx49lmFlYHfm2HWlihd.0lM3kjNxwSM0EzNzEzW}`

Command used: 
`cd /challenge/files`
`/challenge/run *p*`

According the challenge, I had to match every file that contains the letter `p`. 
`*p` matches every file which contain any character before the letter `p`. `p*` matches every character after the letter `p`. Combining both we get `*p*`, which matches every character before and after the letter `p`. 



#6. Mixing globs 

Now, let's put the previous levels together! We put a few happy, but diversely-named files in `/challenge/files`. Go `cd` there and, using the globbing you've learned, write a single, short (6 characters or less) glob that (when passed as an argument to `/challenge/run`) will match the files "challenging", "educational", and "pwning"!

**flag:** `pwn.college{0STUo8ckyvU8LqizzgmIGdDeHVC.QX1IDO0wSM0EzNzEzW}`

Command used: 
`/challenge/run [pce]*`

In this challenge, I had to match the files "challenging", "educational" and "pwning" , by passing an argument which is 6 characters or less. 

From what I learnt from previous challenges, I can mix up globs, so this is how my command looked: 
- `/challenge/run [pce]*`

`[pce]` matches every file starting with letter `p`, `c` or `e`. 
`*` matches every character after the respective letters, which is `p`,`c` or `e`. 

There are only 3 files satisfy that condition, after passing the argument I got the flag.   



#7. Exclusionary globbing 

Armed with this knowledge, go forth to `/challenge/files` and run `/challenge/run` with all files that don't start with `p`, `w`, or `n`!
**NOTE:** The `!` character has a different special meaning in bash when it's not the first character of a `[]` glob, so keep that in mind if things stop making sense! `^` does not have this problem, but is also not compatible with older shells.

**flag:** `pwn.college{Qj4D_3ufT5ldnvHBwMdwmrjj7-m.QX2IDO0wSM0EzNzEzW}`

Command used:
`cd /challenge/files`
`/challenge/run [!pwn]*`

`!` basically excludes the files which start with the given first letters. 
I passed in the above mentioned commands to get the flag. 



#8. Tab Completion 

This challenge has copied the flag into `/challenge/pwncollege`, and you can freely `cat` that file. But you can't type the filename: we used some serious trickery to make sure that you _must_ tab-complete it. Try it out!

flag: `pwn.college{URXdmb6Hl7XJ4lbw1DfsxfS1PJ-.0FN0EzNxwSM0EzNzEzW}`

Command used: `cat /challenge/pwn<tab>`

`<tab>` autocompletes incomplete command passed in the shell. On passing the above mentioned command and pressing tab, I got the flag. 



#9. Multiple options for tab completion 

This challenge has a `/challenge/files` directory with a bunch of files starting with `pwncollege`. Tab-complete from `/challenge/files/p` or so, and make your way to the flag!

**flag:** `pwn.college{0saWNVwhmsq8xHg_ZzcgaA0kAly.0lN0EzNxwSM0EzNzEzW}`

Command used: 
`cat /challenge/files/p<tab>`
`cat /challenge/files/pwncollege-flag`


#10. Tab completion on commands 

Tab completion is for more than files! You can also tab-complete commands. This level has a command that starts with `pwncollege`, and it'll give you the flag. Type `pwncollege` and hit the tab key to auto-complete it!

flag: `pwn.college{E4YliH31vwH8qxjU6TFJ2-QRPEE.0VN0EzNxwSM0EzNzEzW}`

Command used: 
`pwncollege<TAB>`



