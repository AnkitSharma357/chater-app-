# chater-app-
Chat with python

import datetime
import random
greeting=['hi','hello','hye','ok google','good morning','Whats app','gm']
by=['bye','good bye','good night','byy','by']
time=['tell time','time','recent time','date',' today date and  time']
game=['play game','game','play']
shopping=['tv','mobile','earphone']
c=True
while c:
    start=input('Enter your command: ')
    print('_'*20)
    lo=start.lower()
    if lo in greeting:
        print("""
        Hello user 
        how can I help you???""")
        print('_'*20)
    elif lo in time:
        d=datetime.datetime.now().date()
        t=datetime.datetime.now().time()
        print(d)
        print(t)
        print('_'*20)
    elif lo in game:
        cpu=random.randint(1,45)
        print('****GUESS THE NUMBER****')  
        i=1
        while i<=5:
            x=int(input('Guess a number between 1 to 45: '))
            i=i+1
            if x<cpu:
                print('You enter a less number')
                print('_'*20)
            elif x>cpu:
                print('You enter a larger number')
                print('_'*20)
            elif x==cpu:
                print('You win the game....')
                break
        else:
                print('You loss the game number is: ',cpu)
                print('_'*20)
    elif lo in by:
            print('Byy user......')
            c=False
            
                
                
    else:
        print("I dont under stand")
