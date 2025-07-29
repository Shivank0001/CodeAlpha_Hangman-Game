import random

words = ["apple", "banana", "grape", "orange", "mango"]
word = random.choice(words)
guessed_letters = []
tries = 6

print("Welcome to Hangman!")

while tries > 0:
    display_word = ""
    for letter in word:
        if letter in guessed_letters:
            display_word += letter
        else:
            display_word += "_"
    print(display_word)

    if "_" not in display_word:
        print("Congratulations! You guessed the word.")
        break

    guess = input("Guess a letter: ").lower()
    
    if guess in guessed_letters:
        print("You already guessed that letter.")
        continue

    guessed_letters.append(guess)

    if guess not in word:
        tries -= 1
        print(f"Wrong guess. Tries left: {tries}")

if tries == 0:
    print(f"You lost. The word was: {word}")
