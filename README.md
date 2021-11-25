# ROCK_PAPER_SCISSOR_Game
# Python -Rock, paper scissor game 


import random
name = input(" Please enter your name: ")
print("Hello", name + " welcome to our Squid Game of Rock/paper/scissor ")


user_wins = 0
computer_wins = 0
Total_Games = 0

options = ["rock", "paper", "scissors" or "Q"]

while True:

    if computer_wins == 3:
        print(" Oops! you loose")
        break

    if user_wins == 3:
        print("congrats you won")
        break

    user_choice = input(
        "type either rock, paper or scissors or q to quit:").lower()
    if user_choice == "q":
        break

    if user_choice not in options:
        continue

    random_number = random.randint(0, 2)
    # rock= 1, paper =2 and scissors = 3
    Computer_choice = options[random_number]
    print("Computer picked", Computer_choice + " ")
   # condition is possible through switch statement also
   
    if user_choice == "paper" and Computer_choice == "paper":
        print(" Its tie! No One dead, You are still alive")
        continue

    if user_choice == "scissor" and Computer_choice == "scissor":
        print(" Its tie! No One dead, You are still alive")
        continue

    if user_choice == "rock" and Computer_choice == "rock":
        print(" Its tie! No One dead, You are still alive")
        continue

    if user_choice == "rock" and Computer_choice == "paper":
        print(
            "computer won!, you are dead but you still have remaining lifeline, keep it up")
        computer_wins += 1
        continue

    if user_choice == "rock" and Computer_choice == "scissor":
        print("You won!")
        user_wins += 1
        continue

    if user_choice == "scissor" and Computer_choice == "paper":
        print("You won!, you are still alive, you can win the game")
        user_wins += 1
        continue

    if user_choice == "scissor" and Computer_choice == "rock":
        print("user won!, you are dead but you still have remaining lifeline won! ")
        user_wins += 1
        continue

    if user_choice == "paper" and Computer_choice == "scissor":
        print("computer won!, you are dead but you still have remaining lifeline won! ")
        computer_wins += 1
        continue

    if user_choice == "paper" and Computer_choice == "rock":
        print("user won!, you are dead but you still have remaining lifeline won! ")
        user_wins += 1
        continue
    
    print("Goodbye", name + " have a nice day!")
    print("Thank you for playing, Please come again")

