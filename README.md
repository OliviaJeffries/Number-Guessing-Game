#include <stdio.h> 
#include <stdlib.h> 
#include <time.h> 

  int main(void) { 
    int secretNumber; 
    int guess; 
    int attempts = 3; 

// Generate a random number from 1 to 100 
  srand(time(NULL)); 
  secretNumber = rand() % 100 + 1; 

printf("Guess a number between 1 and 100: "); 
scanf("%d", &guess); 
attempts++; 

while (guess != secretNumber)  { 

if (guess < secretNumber) { 
  printf("Too low!\n"); 
} 
else { 
printf("Too high!\n"); 
}  
printf("\nGuess again: "); 
scanf("%d", &guess); 
attempts++; 
} 
printf("Correct!\n"); 
printf("\nYou guessed the number in %d attempts.\n", attempts); 

return 0; 
} 

 
