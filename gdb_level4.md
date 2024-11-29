Executing the file :

![Screenshot 2024-11-29 171859](https://github.com/user-attachments/assets/6be42785-687b-476b-a0b8-4ba013a2d0f4)

After executing the file, gdb took control over this program.

![Screenshot 2024-11-29 171924](https://github.com/user-attachments/assets/83280d75-a1dc-4f11-8c9b-121e79eed83b)

First we need to find where the random value is being set.

so we use "ni" over and over again to go through the program and find where the random value is set.

After this, we set a breakpoint at the address.

![Screenshot 2024-11-29 171840](https://github.com/user-attachments/assets/0a8a5e68-d43a-4b5c-ab11-3889f132b1bc)

We must figure out the series of random values on the stack.

So we used "x/8gx" on rsp to see the values on the stack. x is short for "examine". 8 is the number of values you wanna see. g is short for "giant" and x is for "hex".

After looking at the values, we use "c" to go on.

After the random value is set, we use examine command again.

There will be change in one value because a random value is set.

![Screenshot 2024-11-29 171840](https://github.com/user-attachments/assets/93f2cd75-6104-45d9-b881-fe4356e4c9a4)

Then we use "c" to go through the program.

It asked us to give the random value.

We give the value and then do the same thing over and over again.

At the end, we will get the flag.
