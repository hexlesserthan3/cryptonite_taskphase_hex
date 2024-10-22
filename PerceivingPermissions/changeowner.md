# Changing File Ownership
## Question
In this level, we will practice changing the owner of the /flag file to the hacker user, and then the flag. For this challenge only, I made it so that you can use chown to your heart's content as the hacker user (again, typically, this requires you to be root). Use this power wisely and chown away!


## Solution
![](/images/1.jpg)
1. become the owner of the file using chown
2. make sure i can access the file using ls -l 
3. cat the flag file

flag: pwn.college{I3czAIibK050eB9jVZvBKjNjBuw.dFTM2QDL4kDO1czW}
