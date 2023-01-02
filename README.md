# Rock-Paper-Scissor
import random
Cchoice=["Rock","Paper","Scissor"]
while True:
    print("Rock Paper Scissor Game:")
    youwin,computerwin=0,0
    for i in range(1,6):
        print("Round",i,"Start:")
        print("Please select any one Option:")
        print("1.Rock","2.Paper","3.Scissor",sep='/n')
        Yourchoice=int(input())
        if Yourchoice==1:
            print("You select Rock")
            Yourchoice="Rock"
        elif Yourchoice==2:
            print("You select Paper")
            Yourchoice="Rock"
        elif Yourchoice==3:
            print("You select Scissor")
            Yourchoice="Scissor"
        else:
            print("Invalid Choice")
            break
        Computerchoice=random.choice(Cchoice)
        print("Computer select:",Computerchoice)

        if Yourchoice==Computerchoice:
            youwin+=1
            computerwin+=1
            print("This round is Drawn:")
        elif (Yourchoice=="Paper" and Computerchoice=="Rock") or (Yourchoice=="Rock" and Computerchoice=="Scissor") or (Yourchoice=="Sissor" and Computerchoice=="Paper"):
            youwin+=1
            print("You win this Round")
        else:
            computerwin+=1
            print("Computer win this Round")

    if youwin>computerwin:
        print("You win the Game:")
        print("Score is:","Your Score:",youwin,"Computer Score:",computerwin,sep=" ")
    elif computerwin>youwin:
        print("You lose the Game.Computer win the Game")
        print("Score is:","Your Score:",youwin,"Computer Score:",computerwin,sep=" ")
    else:
        print("Match Drawn")
        print("Score is:","Your Score:",youwin,"Computer Score:",computerwin,sep=" ")
    user_choice=input("Want to Play again?(Yes/Exit)")
    if user_choice=="yes" or user_choice=="Yes" or user_choice=="YES":
        continue
    
    
