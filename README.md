#include<stdio.h>
#include<stdlib.h>
#include<time.h>
int main(void)
{
    int t,w=0,l=0;
    do{
        int i,j;
        float computer=0,player=0,ans1=0,ans2=0;
        srand(time(NULL));
        do{
            player=rand()%13+1;
            if(player==11||player==12||player==13){
                player=0.5;
                ans1+=player;
            }
            else{
                ans1+=player;
            }

            printf("This is your PK %f\n",ans1);
            if(ans1>10.5)
            {
                //printf("you lose\n");
                break;
            }
            printf("Do you want to one more ?\n");
            printf("If you want enter 1 else enter 0\n");
            scanf("%d",&i);

                }
         while(i!=0);
        do{
            computer=rand()%13+1;
            if(computer==11||computer==12||computer==13){
                computer=0.5;
                ans2+=computer;
            }
            else {
                ans2+=computer;

            }
            if(ans2<=7) j =1;
                else j = 0;
        }while(j!=0);
        //printf("%d",ans1);

        printf("This is mine %f\n",ans2);
        if(ans1>ans2&&ans1<=10.5){printf("Your win!\n");
        w++;}
        else if(ans2>10.5){printf("Your win!\n");
        w++;}
        else{ printf("Your lose!\n");
        l++;}
        printf("Do you want to play again?(if you want please enter 1 else enter 0)\n");
        scanf("%d",&t);
    }while(t!=0);
    printf("You win %d time\n",w);
    printf("You lose %d time\n",l);
    return 0;
}
