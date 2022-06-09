# Rock-paper-scissors-game
This is a game between random guesses of player and computer
#first is to import random

import random
print('Welcome to my game called *Rock, Paper, Scissors*')
player_wins = 0
CPU_wins = 0
#represent the elements in a list


options = ['R', 'P', 'S']
#where R: Rock, P: Paper and S: scissors
while True:
    player_input = input('Type in R/P/S or Q to quit: ')#.lower()
    if player_input == 'q':
        break

    if player_input not in options:
        print('The letter you typed is not in the options, please type either R, P, S')
        continue

    random_number = random.randint(0, 2)
    #this represent position of rock, paper, scissors
    CPU_picks = options[random_number]
    print('Computer picked', CPU_picks + '.')

    if player_input == 'R' and CPU_picks == 'S':
        print('You won congratulations!')
        player_wins += 1

    elif player_input == 'P' and CPU_picks == 'R':
        print('You won congratulations!')
        player_wins += 1

    elif player_input == 'S' and CPU_picks == 'P':
        print('You won congratulations!')
        player_wins += 1

    elif player_input == 'R' and CPU_picks == 'R':
        print('There is a tie!')
        player_wins += 0
    elif player_input == 'P' and CPU_picks == 'P':
        print('There is a tie!')
        player_wins += 0
    elif player_input == 'S' and CPU_picks == 'S':
        print('There is a tie!')
        player_wins += 0

    else:
        print('You lost the game!')
        CPU_wins += 1


print('You won', player_wins, 'times.')
print('Computer won the game', CPU_wins, 'times.')

print('Goodbye, thanks for your time')

