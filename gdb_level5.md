To execute the file :



I solved this in 2 ways.

Script 1 :

![image](https://github.com/user-attachments/assets/85382f49-77b5-4d9f-a45e-4deb16a8059c)

We should first check where the random value is being set. Then we should set a breakpoint there.

Here it is main+721. After setting the breakpoint, we used "commands" and wrote some code in it. 

This code gets executed whenever the breakpoint is hit. Here, whenever the breakpoint is hit, I printed the random values in the stack. 

As ik where the random value is, I will copy it and paste it when it asks us for the random value.

Since there is a series of random values, we need to enter them again and again. We will get the flag. (kinda long)

Script 2 :

![image](https://github.com/user-attachments/assets/8aa8a463-10ed-4624-b229-8142dea104e3)

After setting the breakpoint, we used "silent" just to keep our output clean.

Then we used the set command to set the value at 40 bytes after rsp (Our random value) to 0.

Then we used "continue" so that it will just ask us for the random value. 

Now, since we know the random value, which is zero, we don't need to check it's value. We can just print 0 whenever it asks us for the random value. 

Giving the input as zero whenever it asks us for the random value gives the flag.

Or you can just give the input as 0 in the first try and then give anything else in the second try, it will directly lead us to the flag since the challenge is kinda broken.

