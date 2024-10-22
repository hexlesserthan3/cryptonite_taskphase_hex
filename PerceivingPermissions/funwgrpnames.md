# Fun with Group Names
## Question
In this challenge, you must retrieve the exit code returned by /challenge/get-code and then run /challenge/submit-code with that error code as an argument. Good luck!


## Solution
![](/images/3.jpg)
1. find the name of the group that contains our user
2. use chgrp to gain access to the group that our user is a part of
3. get the flag using cat

flag: pwn.college{U88fD2Fzy1yItXSvcXe76KcSTxl.dJzNyUDL4kDO1czW}
