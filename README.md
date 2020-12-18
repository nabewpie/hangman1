import random
print("Let's Play")
words = ["games", "daddy", "later", "early"]
words_list = random.choice(words)
words_length = len(words_list)
words_element = (words_list[0],words_list[1],words_list[2], words_list[3], words_list[4]) 
print(words_element)
input_alpha = input("letter : ")

if input_alpha == words_list[0]:
    print("ok")
if input_alpha == words_list[1]:
    print("ok")
if input_alpha == words_list[2]:
    print("ok")
if input_alpha == words_list[3]:
    print("ok")
if input_alpha == words_list[4]:
    print("ok")
if input_alpha != words_list[0]:
    print("ded")
if input_alpha != words_list[1]:
    print("ded")
if input_alpha != words_list[2]:
    print("ded")
if input_alpha != words_list[3]:
    print("ded")
if input_alpha != words_list[4]:
    print("ded")
