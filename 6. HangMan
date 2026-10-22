import random

stages = [
    '''
       +---+
       |   |
       O   |
      /|\\  |
      / \\  |
           |
    =========
    ''',
    '''
       +---+
       |   |
       O   |
      /|\\  |
      /    |
           |
    =========
    ''',
    '''
       +---+
       |   |
       O   |
      /|\\  |
           |
           |
    =========
    ''',
    '''
       +---+
       |   |
       O   |
       |   |
           |
           |
    =========
    ''',
    '''
       +---+
       |   |
       O   |
           |
           |
           |
    =========
    ''',
    '''
       +---+
       |   |
           |
           |
           |
           |
    =========
    '''
]

word_list = ["apple", "banana", "orange", "python", "computer"]

chosen_word = random.choice(word_list)
word_length = len(chosen_word)

display = []

for _ in range(word_length):
    display.append("_")

lives = 5
guessed_letters = []

print("Welcome to Hangman!")
print(" ".join(display))

game_over = False

while not game_over:

    guess = input("Guess a letter: ").lower()

    if guess in guessed_letters:
        print(f"You already guessed {guess}.")
        continue

    guessed_letters.append(guess)

    if guess in chosen_word:

        for position in range(word_length):
            letter = chosen_word[position]

            if letter == guess:
                display[position] = guess

    else:
        lives -= 1
        print(f"You guessed {guess}, that's not in the word.")

    print(stages[lives])
    print(" ".join(display))

    if "_" not in display:
        game_over = True
        print("You win! 🎉🥳")

    if lives == 0:
        game_over = True
        print(f"You lose! The word was {chosen_word}.")
