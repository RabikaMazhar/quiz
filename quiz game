#include <stdio.h>
#include <stdlib.h>
#include <time.h>
#include <ctype.h>
char name[30];
int userScore = 0, countQ = 0;
int questionOrder[10] = {0, 1, 2, 3, 4, 5, 6, 7, 8, 9};
int previousScore = 0;
void menu();
void calculateScore();
char result(char choose, char correct);
void question(int questionIndex);
void shuffleQuestions();
void calculateScore()
{
system("cls");
// Calculation of score and feedback based on user's performance
if (userScore >= 40 && userScore <= 100)
{
printf("***************************************\n");
printf("\nCongrats, %s! You win the quiz.\n", name);
printf("You scored %d out of 100.\n", userScore);
printf("You answered %d questions correctly.\n", countQ);
printf("***************************************\n");
}
else if (userScore >= 10 && userScore < 40)
{
printf("***************************************\n");
printf("Sorry, %s! You lost the quiz.\n", name);
printf("You scored %d out of 100.\n", userScore);
printf("You answered %d questions correctly.\n", countQ);
printf("Better luck next time!\n");
printf("***************************************\n");
}
printf("\nIf you want to retake the quiz, enter 'R'. ");
printf("To exit, press any other key.\n");
char retake;
while ((getchar()) != '\n')
;
scanf(" %c", &retake);
if (retake == 'R' || retake == 'r')
{
previousScore = userScore; // Store the current score as the previous 
score
userScore = 0;
countQ = 0;
printf("\n");
menu();
}
else
{
exit(0);
}
}
char result(char choose, char correct)
{
char next;
choose = toupper(choose); // Convert user's input to uppercase
correct = toupper(correct); // Convert correct answer to uppercase
if (choose == 'A' || choose == 'B' || choose == 'C' || choose == 'D')
{
if (choose == correct)
{
countQ++;
userScore = userScore + 10;
printf("Your answer is correct!\n");
}
else
{
printf("Sorry, the answer is wrong!\n");
// printf("Correct answer is: '%c'\n", correct);
}
printf("Press (Y) to continue the quiz. ");
printf("If you want to end the quiz, press (N)\n");
while ((getchar()) != '\n')
;
scanf(" %c", &next);
}
else
{
printf("Invalid input! Please choose a valid option (A, B, C, or D).\n");
printf("Press (Y) to continue the quiz. ");
printf("If you want to end the quiz, press (N)\n");
while ((getchar()) != '\n')
;
scanf(" %c", &next);
}
return next;
}
void question(int questionIndex)
{
char choose, correct;
if (questionIndex == 0)
{
system("cls");
printf("Q-Which data type stores characters?\n");
printf("\t(A) Int\t(B) Float\n");
printf("\t(C) Char\t(D) Byte\n");
printf("Choose the correct option: ");
while ((getchar()) != '\n')
;
scanf(" %c", &choose);
correct = 'C';
correct = result(choose, correct);
}
else if (questionIndex == 1)
{
system("cls");
printf("Q-Which function is used to read a character from the standard 
input?\n");
printf("\t(A) getchar()\t(B) scanf()\n");
printf("\t(C) read()\t(D) fgets()\n");
printf("Choose the correct option: ");
while ((getchar()) != '\n')
;
scanf(" %c", &choose);
correct = 'A';
correct = result(choose, correct);
}
else if (questionIndex == 2)
{
system("cls");
printf("Q-How do you access the elements of an array?\n");
printf("\t(A) Using parentheses () \t(B) Using square brackets []\n");
printf("\t(C) Using curly braces {}\t(D) Using angle brackets <>\n");
printf("Choose the correct option: ");
while ((getchar()) != '\n')
;
scanf(" %c", &choose);
correct = 'B';
correct = result(choose, correct);
}
else if (questionIndex == 3)
{
system("cls");
printf("Q-Which header file should be included to work with dynamic 
memory allocation in C?\n");
printf("\t(A) stdio.h \t(B) math.h\n");
printf("\t(C) string.h\t(D) stdlib.h\n");
printf("Choose the correct option: ");
while ((getchar()) != '\n')
;
scanf(" %c", &choose);
correct = 'D';
correct = result(choose, correct);
}
else if (questionIndex == 4)
{
system("cls");
printf("Q-Which loop allows the code to be executed at least once, even 
if the condition is false?\n");
printf("\t(A) for loop \t(B) while loop\n");
printf("\t(C) do-while loop\t(D) if-else statement\n");
printf("Choose the correct option: ");
while ((getchar()) != '\n')
;
scanf(" %c", &choose);
correct = 'C';
correct = result(choose, correct);
}
else if (questionIndex == 5)
{
system("cls");
printf("Q-Which type of values are stored in the Int data type?\n");
printf("\t(A) Integer\t(B) Floating point\n");
printf("\t(C) Character\t(D) String\n");
printf("Choose the correct option: ");
while ((getchar()) != '\n')
;
scanf(" %c", &choose);
correct = 'A';
correct = result(choose, correct);
}
else if (questionIndex == 6)
{
system("cls");
printf("Q-Which type of values are stored in the Float datatype?\n");
printf("\t(A) Integer\t(B) Floating point\n");
printf("\t(C) Character\t(D) String\n");
printf("Choose the correct option: ");
while ((getchar()) != '\n')
;
scanf(" %c", &choose);
correct = 'B';
correct = result(choose, correct);
}
else if (questionIndex == 7)
{
system("cls");
printf("Q-Which type of values are stored in the Double data type?\n");
printf("\t(A) Integer\t(B) Floating point\n");
printf("\t(C) Character\t(D) String\n");
printf("Choose the correct option: ");
while ((getchar()) != '\n')
;
scanf(" %c", &choose);
correct = 'B';
correct = result(choose, correct);
}
else if (questionIndex == 8)
{
system("cls");
printf("Q-What is a string?\n");
printf("\t(A) Integer values \t(B) Floating values\n");
printf("\t(C) Character array\t(D) Array\n");
printf("Choose the correct option: ");
while ((getchar()) != '\n')
;
scanf(" %c", &choose);
correct = 'C';
correct = result(choose, correct);
}
else if (questionIndex == 9)
{
system("cls");
printf("Q-What is a structure?\n");
printf("\t(A) Integer\t(B) Float\n");
printf("\t(C) Character\t(D) User-defined data type\n");
printf("Choose the correct option: ");
while ((getchar()) != '\n')
;
scanf(" %c", &choose);
correct = 'D';
correct = result(choose, correct);
}
if (correct == 'n' || correct == 'N')
{
calculateScore();
}
}
void shuffleQuestions()
{
// Shuffle the question order using Fisher-Yates algorithm
for (int i = 9; i > 0; i--)
{
int j = rand() % (i + 1);
int temp = questionOrder[i];
questionOrder[i] = questionOrder[j];
questionOrder[j] = temp;
}
// Present questions in the shuffled order
for (int i = 0; i < 10; i++)
{
question(questionOrder[i]);
}
}
void menu()
{
char ch;
system("cls");
printf("\nHello! %s\n", name);
if (previousScore != 0)
{
printf("Your previous score: %d\n", previousScore);
}
printf("Here are some rules of this Game.\n");
printf("1. You can choose any option.\n");
printf("2. You need to answer 10 questions.\n");
printf("3. Each question is worth 10 points.\n");
printf("4. Total score is out of 100.\n");
printf("5. We will determine if you win the quiz or not.\n");
printf("Press (Y) to start the quiz, otherwise press (N)\n");
while ((getchar()) != '\n')
;
scanf(" %c", &ch);
if (ch == 'y' || ch == 'Y')
{
shuffleQuestions();
calculateScore();
}
else
{
exit(0);
}
}
int main()
{
system("cls");
printf("\n**Welcome to the Quiz Game\n");
printf("Enter your name: ");
scanf("%s", name);
menu();
return 0;
}
