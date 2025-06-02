stages=['''
        ----------
             |    |
             |    |
             O    |
            /|\   |
            / \   |
                  |
                  |
        ''',
        '''
        ----------
             |    |
             |    |
             O    |
            /|\   |
            /     |
                  |
                  |
        ''',
        '''
        ----------
             |    |
             |    |
             O    |
            /|\   |
                  |
                  |
                  |
        ''',
        '''
        ----------
             |    |
             |    |
             O    |
            /|    |
                  |
                  |
                  |
        ''',
        '''
        ----------
             |    |
             |    |
             O    |
             |    |
                  |
                  |
                  |
        ''',
        '''
        ----------
             |    |
             |    |
             O    |
                  |
                  |
                  |
        ''',
        '''
        ----------
             |    |
             |    |
                  |
                  |
                  |
                  |
        ''']
import random
l1=["apple","banana","guvava","grapes"]
computer_choice=random.choice(l1)
# print(computer_choice)
l2=[]
for i in range(len(computer_choice)):
    l2.append("_")
print(l2)
life=6
game_over=False
while not game_over:
    guess=input("try to guess the letter in word")
    for i in range (len(computer_choice)):
        if (computer_choice[i]==guess):
            l2[i]=guess
    print(l2)
   # print(life)
    if guess not in computer_choice:
        life-=1
        if life==0:
          print("game over you loose the game")
          game_over=True
    if "_" not in l2:
        print("you won the game in life",life)
        game_over=True
    print(life)
    print(stages[life])
print(l2)
