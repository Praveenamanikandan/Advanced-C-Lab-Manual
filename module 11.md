## Name: Praveena M
## Reg No: 212223040153

## EXP NO:21 C PROGRAM TO CREATE A FUNCTION TO FIND THE GREATEST NUMBER
## Aim:
To write a C program to create a function to find the greatest number

## Algorithm:
1.	Include the necessary header #include <stdio.h>.
2.	Use a series of if and else if statements to compare the values and return the maximum among them.
3.	Declare variables n1, n2, n3, n4, and greater to store user input and the result.
4.	Use scanf to take four integers as input.
5.	Call the max_of_four function with the input integers and store the result in the greater variable
 
## Program:
```
#include <stdio.h>

int max_of_four(int a, int b, int c, int d) {
    if (a >= b && a >= c && a >= d) {
        return a;
    } else if (b >= a && b >= c && b >= d) {
        return b;
    } else if (c >= a && c >= b && c >= d) {
        return c;
    } else {
        return d;
    }
}

int main() {
    int n1, n2, n3, n4, greater;

    printf("Enter four integers: ");
    scanf("%d %d %d %d", &n1, &n2, &n3, &n4);

    greater = max_of_four(n1, n2, n3, n4);

    printf("The greatest number is: %d\n", greater);

    return 0;
}








```

## Output:
![image](https://github.com/user-attachments/assets/6a6df717-0249-4152-9b4e-6410cc40531a)


## Result:
Thus, the program  that create a function to find the greatest number is verified successfully.


 
## EXP NO:22 C PROGRAM TO PRINT THE MAXIMUM VALUES FOR THE AND, OR AND  XOR COMPARISONS
## Aim:
To write a C program to print the maximum values for the AND, OR and XOR comparisons

## Algorithm:
1.	Define a function calculate_the_max that takes two integers n and k as parameters.
2.	Declare variables a, o, and x to store the maximum values for AND, OR, and XOR operations, respectively.
3.	Use nested loops to iterate through pairs of integers (i, j) from 1 to n.
4.	Within the loops, check conditions for AND, OR, and XOR operations and update the corresponding maximum values (a, o, x).
5.	Declare variables n and k to store user input.
6.	Use scanf to take two integers as input.
7.	Call the calculate_the_max function with input values.
 
## Program:
```
#include <stdio.h>

void calculate_the_max(int n, int k) {
    int a = 0, o = 0, x = 0;

    for (int i = 1; i <= n; i++) {
        for (int j = i + 1; j <= n; j++) {
            int and_result = i & j;
            int or_result = i | j;
            int xor_result = i ^ j;

            if (and_result < k && and_result > a) {
                a = and_result;
            }
            if (or_result < k && or_result > o) {
                o = or_result;
            }
            if (xor_result < k && xor_result > x) {
                x = xor_result;
            }
        }
    }

    printf("Maximum AND value: %d\n", a);
    printf("Maximum OR value: %d\n", o);
    printf("Maximum XOR value: %d\n", x);
}

int main() {
    int n, k;

    printf("Enter two integers (n and k): ");
    scanf("%d %d", &n, &k);

    calculate_the_max(n, k);

    return 0;
}









```

## Output:
![image](https://github.com/user-attachments/assets/86dd602c-e318-4f0e-bc50-72cdcdb04e0e)


## Result:
Thus, the program to print the maximum values for the AND, OR and XOR comparisons
is verified successfully.


 
## EXP NO:23 C PROGRAM TO WRITE THE LOGIC FOR THE REQUESTS
## Aim:
To write a C program to write the logic for the requests

## Algorithm:
1.	Declare variables noshel and noque to store the number of shelves and the number of queries, respectively.
2.	Use scanf to take two integers as input for the number of shelves and queries.
3.	Declare a 2D array shelarr to represent shelves and books, and an array nobookarr to store the number of books on each shelf.
4.	Declare variables k and c to keep track of the book index and the total number of books.
5.	Use a for loop to iterate over the queries.
 
## Program:
```

#include <stdio.h>

int main() {
    int noshel, noque;

    printf("Enter the number of shelves and number of queries: ");
    scanf("%d %d", &noshel, &noque);

    int shelarr[noshel][100];
    int nobookarr[noshel];

    for (int i = 0; i < noshel; i++) {
        nobookarr[i] = 0;
    }

    for (int q = 0; q < noque; q++) {
        int query_type;
        printf("Enter query type (1 for add, 2 for remove, 3 for display): ");
        scanf("%d", &query_type);

        if (query_type == 1) {
            int shelf, book_count;
            printf("Enter shelf index and number of books to add: ");
            scanf("%d %d", &shelf, &book_count);
            
            if (shelf >= 0 && shelf < noshel) {
                for (int i = nobookarr[shelf]; i < nobookarr[shelf] + book_count; i++) {
                    shelarr[shelf][i] = i + 1;
                }
                nobookarr[shelf] += book_count;
                printf("Added %d books to shelf %d\n", book_count, shelf);
            } else {
                printf("Invalid shelf index.\n");
            }
        } 
        else if (query_type == 2) {
            int shelf, book_count;
            printf("Enter shelf index and number of books to remove: ");
            scanf("%d %d", &shelf, &book_count);
            
            if (shelf >= 0 && shelf < noshel) {
                if (book_count <= nobookarr[shelf]) {
                    nobookarr[shelf] -= book_count;
                    printf("Removed %d books from shelf %d\n", book_count, shelf);
                } else {
                    printf("Not enough books to remove from shelf %d\n", shelf);
                }
            } else {
                printf("Invalid shelf index.\n");
            }
        }
        else if (query_type == 3) {
            int shelf;
            printf("Enter shelf index to display: ");
            scanf("%d", &shelf);

            if (shelf >= 0 && shelf < noshel) {
                printf("Books on shelf %d: ", shelf);
                for (int i = 0; i < nobookarr[shelf]; i++) {
                    printf("%d ", shelarr[shelf][i]);
                }
                printf("\n");
            } else {
                printf("Invalid shelf index.\n");
            }
        }
    }

    return 0;
}

```


## Output:

![image](https://github.com/user-attachments/assets/cbe88521-d264-4ef6-b967-efd3bd64f49e)


## Result:
Thus, the program to write the logic for the requests is verified successfully.


 
## EXP NO:24 C PROGRAM PRINT THE SUM OF THE INTEGERS IN THE ARRAY.
## Aim:
To write a C program print the sum of the integers in the array.

## Algorithm:
1.	Declare a variable n to store the number of integers.
2.	Use scanf to take an integer n as input.
3.	Declare an array a of size n to store the integers.
4.	Declare a variable sum and initialize it to zero.
5.	Use a for loop to iterate n times:
6.	Use scanf to input each integer and add it to the sum.
7.	Print the final sum using printf.



## Program:
```

#include <stdio.h>

int main() {
    int n, sum = 0;

    printf("Enter the number of integers: ");
    scanf("%d", &n);

    int a[n];

    printf("Enter %d integers: ", n);
    for (int i = 0; i < n; i++) {
        scanf("%d", &a[i]);
        sum += a[i];
    }

    printf("Sum of the integers: %d\n", sum);

    return 0;
}








```

## Output:
![image](https://github.com/user-attachments/assets/4d236e95-9051-49a5-8648-696a563d29b9)


 


## Result:
Thus, the program prints the sum of the integers in the array is verified successfully.


 
## EXP NO 25: C PROGRAM TO COUNT THE NUMBER OF WORDS IN A      SENTENCE



## Aim:

To write a C program that counts the number of words in a given sentence.

## Algorithm:

1.	Input the sentence: Take a sentence from the user.
2.	Initialize a counter variable: This will keep track of the number of words.
3.	Process each character of the sentence:
o	Iterate through the sentence, checking each character.
o	If a character is not a space, it may belong to a word. If it's the first non-space character after a space or at the start, increment the word count.
4.	Handle spaces and punctuation: Skip over spaces, punctuation marks, and consider each word as a sequence of characters separated by spaces.
5.	Display the result: After processing the sentence, output the total word count.



## Program:
```

#include <stdio.h>
#include <ctype.h>

int countWords(char sentence[]) {
    int count = 0;
    int inWord = 0;

    for (int i = 0; sentence[i] != '\0'; i++) {
        if (isspace(sentence[i]) || sentence[i] == '.' || sentence[i] == ',' || sentence[i] == ';' || sentence[i] == '!') {
            inWord = 0;
        } else {
            if (inWord == 0) {
                count++;
                inWord = 1;
            }
        }
    }

    return count;
}

int main() {
    char sentence[1000];

    printf("Enter a sentence: ");
    fgets(sentence, sizeof(sentence), stdin);

    int wordCount = countWords(sentence);
    printf("The number of words in the sentence is: %d\n", wordCount);

    return 0;
}


```

## Output:


![image](https://github.com/user-attachments/assets/f26ef9fe-e0d1-4893-8c61-7f02a109be02)



## Result:

Thus, the program that counts the number of words in a given sentence is verified 
successfully.
