# Epic Filesystem Quest
## Question
In this challenge, I have hidden the flag! Here, you will use ls and cat to follow my breadcrumbs and find it! Here's how it'll work:

   1. Your first clue is in /. Head on over there.
   2. Look around with ls. There'll be a file named HINT or CLUE or something along those lines!
   3. cat that file to read the clue!
   4. Depending on what the clue says, head on over to the next directory (or don't!).
   5. Follow the clues to the flag!

Good luck!


## Solution
![](/images/91.jpg)
![](/images/92.jpg)
![](/images/93.jpg)
![](/images/94.jpg)
1. basically just a long list of changing looking into directories
2. hidden directories had a . before the file path
3. trapped directories were accessed without changing into them
4. regular directories used: cd and ls
5. final file was in the /usr directory under the name .BRIEF

flag: pwn.college{snqJNxGEB7JxNqTa8pS0fv6Nq5I.dljM4QDL4kDO1czW}
