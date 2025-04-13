import random

def number_guessing_game():
    print("Welcome to the Number Guessing Game!")
    print("I'm thinking of a number between 1 and 100.")

    guessing_number = random.randint(1, 100)
    guess = None
    attempts = 0

    while guess != guessing_number:
        try:
            guess = int(input("Guess a number between 1 and 100: "))
            attempts += 1

            if guess < guessing_number:
                print("Too low.")
            elif guess > guessing_number:
                print("Too high.")
            else:
                print(f"Congratulations! You guessed it in {attempts} tries.")
        except ValueError:
            print("Please enter a valid number.")


number_guessing_game()
