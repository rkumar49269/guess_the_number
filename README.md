# guess_the_number
// a simple program made while practising with the help of code with harry.

#include <stdio.h>
#include <conio.h>
#include <stdlib.h>
#include <time.h>

int main(){
    int num,guess,nguesses=1;
    srand(time(0)); // to generate random numbers.
    num = rand()%100 + 1;  //to a range of 100 for the random number. 
    // printf("\nThe random number is %d\n", num);
    // wanted to guess the random generated number to be guess atleast once.
    do{
        printf("Enter the guessed number\n");
        scanf("%d",&guess); // user input for guessed number.
        // condition check whether the number entered by  the user is less, greater or equal.
        if(guess<num){
            printf("Guess higher number please!\n");
        }
        else if (guess>num){
            printf("Guess lower number please!\n");
        }
        else{
            printf("You guessed it in %d Attempts!", nguesses);
        }
        nguesses++;  // number of guesses increases after every failed attempts.
    } while (guess!=num);
    // here the program ends.
    return 0;
}
