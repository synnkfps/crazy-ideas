# crazy ideas: powered by Brain

### Anamorphic String Obfuscator
hard to explain but, it would create a backend 2d box, you will "throw" your string letters in it, then the box starts to getting swapped (like 2048 game) so the character index of the letters gets assembled, at the end, you will probably get a big number <br>
then it will have some (also crazy) settings:
- backend model
  - triangle, square, cube
- string income type
  - bytes, alphabet index, square root of its index, disassembled shuffled bytes
  - shuffled power of itself (also bytes)
- backend model size
  - sets the size of the model, more = less obfuscation

#### how it would work
creates a backend model, you wont see it, for example:
```
#############          #
#           #         # #
#           #        #   #
#           #  or   #     #
#           #      #       #
#           #     #         #
#############    #############
```
the string letters will be throwed randomly
```
#############          
#        o  #        
#  l        #        
#     e     #  string: hello
#           # 
# h   l     #
#############
```
then it will swap X times (it will be randomy generated),
then for each number in the current number, it will select a random number between 1 to 4

1234 = 1: left, 2: up, 3: down, 4: right

then it will swap. The final string will be intelligently randomized, at the final you will get the bytes of each letter of the final output, example:
```
lhloe = 6c 68 6c 6f 65
then replacing letters
63 68 63 66 65 
shuffled: 63 66 65 68 63 (can aldo be not shuffled)
then multiplying:
63*68*63*66*65 = 1157836680
separe each 2 = 11 57 83 66 80
then we replace them for each alphabet index:
aa eg hc ff h = aaeghcffh = hello
```

