/* C program to design a digital clock */

#include <stdio.h>
#include <time.h> // for sleep () function
#include <unistd.h>
#include <stdlib.h>
int main() 
{
    int hours, minutes, seconds;
    hours=minutes=seconds= 0;
    while(1)
    {
        // clear output screen
        system("cls");
        // print time in HH:MM:SS format
        printf("%02d : %02d : %02d", hours, minutes, seconds);
        // clear output buffer in gcc
    fflush(stdout);
    // increase seconds
    seconds ++ ;
    // update hours, minutes, and seconds
    if(seconds == 60)
    {
        minutes+=1;
        seconds=0;
    }
    if(minutes == 60)
    {
        hours+=1;
        minutes=0;
    }
    if(hours == 24)
    {
        hours=0;
        minutes=0;
        seconds=0;
    }
    sleep(1); // wait for 1 second
    }
    return 0;
}


    
        
    
