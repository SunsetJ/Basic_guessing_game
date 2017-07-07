# Basic_guessing_game
# A guessing game using basic python 

import random as r

print("Hello and welcome to the guessing game!")

def num_check(question):
    valid = False
    while not valid:
        try:
            response = int(input(question))
            valid = True
            return response
        except ValueError:
            print("Please enter a number")

def guess_again():
    valid = False
    while not valid:
        guess = num_check("Guess again!")
        check_guess()

def check_guess():
    if guess < num:
        print("Your guess was {}, which is too low!".format(guess))
        guess_again()
    elif guess > num:
        print("Your guess was {}, which is too high!".format(guess))
        guess_again()
    elif guess == num:
        print("You got it!! That was the correct number!!")

for a in range(0,3):
    print("Round {}:".format(a+1))
    guess = num_check("Guess a number between 1 and 10!")
    num = r.randint(1, 10)
    check_guess()
