# block-chat
while creating some simple tasks for my brother to help him learn to code, i stumbled across the turbowarp mod and when i found out that you can even use cloud data functionality, i just had to try it out myself!   

the limitations of scratch cloud data is simple, it can only store numbers, not strings   

that means that we have to encode each message by just 10 digits,
1234567890
the problem is that we need a separator
some information of where the first number ends and the second starts

I managed to create super simple codec (encoder/decoder) that stores the data accordingly 

xxxxxx0xxxxx
the number on the left is index of the letter in the dictionary,
the "0" is the separator, it is the first "0" from the right
the numbers on the right are simply how many digits each index number has.
(we know that it has to be >0)

example

lets say we have dictionary   
abcd...xyz  

"a" with index 1, 
b index 2, 
y 25 etc

if i want to send the "abzc"
the encoder output would be
12263 0 1121

to decode it, i first find the on the very right 0, that's a separator   
the clever ones will understand that this way, the largest index we can store is    
999999999, (being the highest 9 digit number) but that's plenty of characters imo :D   

it's not a rocket science id say, literally programming for kids lol,   

i guess that's it, i tend to overcomplicate simple things, maybe rather feel free to look at the code yourself

love,  
Cubiq

