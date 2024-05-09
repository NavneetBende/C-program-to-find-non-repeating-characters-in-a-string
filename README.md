Finding non repeating characters in a string.
In this article we will learn how to code a C program to find non repeating characters in a string. Non repeating characters are those that are present in the string only once. To find non repeating characters in a string we will use one for loop to calculate the frequency of each character and print those characters that have frequency count one using another for loop.

C program to find non repeating characters in a string in C
Algorithm:
Initialize the variables.
Accept the input.
Initialize a for loop and terminate it at the end of string. 
This for loop will calculate the frequency of each character.
Print the characters having frequency one.
While loop in C
C Code For Finding Non Repeating Characters
#include<stdio.h> 
int main()
{
    //Initializing variables.
    char str[100]="prepinsta";
    int i;
    int freq[256] = {0};
    //Calculating frequency of each character.
    for(i = 0; str[i] != '\0'; i++)
    {
        freq[str[i]]++;
    }
 printf("The non repeating characters are: ");
  for(i = 0; i < 256; i++)
  {
    if(freq[i] == 1)//Finding uniques charcters and printing them.
     {
      printf(" %c ", i);
     }
  }
  return 0;
 }
output
The non repeating characters are: a e i n r s t
