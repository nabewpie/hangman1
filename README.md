import random
print("Let's Play")
letters_guessed = []
tries = 7

words = ["games", "jumpy", "later", "early", "haunt", "blown", "bluer", "bedim", "beano", "letter"]
password = ["hangman", "noose", "gallows", "cool", ""]
chosen_word = random.choice(words)
chosen_pass = random.choice(password)
words_length = len(chosen_word)
blank = "*" * len(chosen_word)

print("To reveal letter, guess the password. WARNING! Wrong password may cost you a life!! Passwords = hangman, noose, gallows, cool")

words_as_list = list(chosen_word)

while tries > 0:
    guess = input("Letter : ").lower()
    
    
    
    if guess == "":
        print("Enter a  letter, not the Enter key!!")
        tries =+ 0
    if guess in words_as_list and guess not in letters_guessed:
        letters_guessed.append(guess)
        
        chosen_word_list = list(chosen_word)
        for i in range (0, len(chosen_word)):
            if words_as_list[i] == guess:
                l = list(blank)
                l[i] = guess
                blank = "".join(l)
                print (blank)
        

    elif guess == str(chosen_pass):
        print(chosen_word)
        
        
        
    else:
        print("Wrong")
        tries -= 1
        print("Number of Tries : " + str(tries))
        
    


    if tries > 0 and blank == chosen_word:
        print("YOU  WON!!!!!")
    
    
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
              |     /
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
              |     / \
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
              |     / \
         ----------
         ''')
   
    

        
else:
    print("lol you lose")

    
    
