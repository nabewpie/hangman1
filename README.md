import random
print("Let's Play")
letters_guessed = []
tries = 7
words = ["games", "jumpy", "later", "early", "haunt", "blown", "bluer", "bedim", "beano"]
words_list = random.choice(words)
words_length = len(words_list)
words_element = (words_list[0],words_list[1],words_list[2], words_list[3], words_list[4], ) 
while tries > 0:
    guess = input("letter : ").lower()
    word_as_list = list
    
    if guess == "":
        print("A letter!!")
    
    if guess in words_list:
        print("Correct")
        letters_guessed.append(guess)
        print("Letters guessed" + str(letters_guessed))
    else:
        print("Wrong")
        tries -= 1
        print("Number of Tries :" + str(tries))
    if tries == 6:
        print('''
              ----------
              |        |
              |        |
              |        |
              |
              |
              |
         ----------
         ''')
    if tries == 5:
        print('''
              ----------
              |        |
              |        |
              |        |
              |     {[]}
              |
              |
              |
         ----------
         ''')
    if tries == 4:
        print('''
              ----------
              |        |
              |        |
              |        |
              |     {[]}
                     |
              |      |
              |      |
              |
         ----------
         ''')
    if tries == 3:
        print('''
              ----------
              |        |
              |        |
              |        |
              |     {[]}
                     |
              |     \|
              |      |
              |      
         ----------
         ''')
    if tries == 2:
        print('''
              ----------
              |        |
              |        |
              |        |
              |     {[]}
                     |
              |     \|/
              |      |
              |      
         ----------
         ''')
    if tries == 1:
        print('''
              ----------
              |        |
              |        |
              |        |
              |     {[]}
                     |
              |     \|/
              |      |
              |      /
         ----------
         ''')
    if tries == 0:
        print('''
              ----------
              |        |
              |        |
              |        |
              |     {[]}
                     |
              |     \|/
              |      |
              |      /\
         ----------
         ''')
    if tries == 0:
        print('''
              ----------
              |        |
              |        |
              |        |                   0    0
              |     {[]}     | /    000
                     |       |/    |   |    ----
              |     \|/      |\    |   |   -    -
              |      |       | \    000
              |      /\
         ----------
         ''')
   
    

        
else:
    print("lol you lose")

