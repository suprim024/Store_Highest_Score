# Store_Highest_Score
# this program generates a random score and compares it with the high score stored in a file.   

import random

def high_score():
    score=random.randint(1,100)
    with open("highscore.txt") as f:
        highscore=f.read()
        if highscore!="":
            highscore=int(highscore)
            
        else:
            highscore=0
    
    # Compare the generated score with the high score   
    print("Your score is:", score)      
    if (score > int(highscore)):
        
        print("Congratulations! You have a new high score:", score)
        with open("highscore.txt","w") as f:
            f.write(str(score))
    else:
        print("You did not beat the high score of:", highscore)         
high_score()
