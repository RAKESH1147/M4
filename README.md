# EX-16-LEFT-SHIFT-OPERATION
## AIM
To write a C Program to perform the basic left shift operation for 44 integer number with 3 shifts.

## ALGORITHM
1.	Start the program.
2.	Assign values of a and b as 44 and 3.
3.	Use left shift operator (<<) and shift the value of a three times.
4.	Display the result.
5.	Stop the program.

## PROGRAM
``` c
#include <stdio.h>

int main() {
    int a = 44; 
    int b = 3;  
    int result = a << b;

    printf("The result of left shifting %d by %d positions is: %d\n", a, b, result);

    return 0;
}

```
## OUTPUT

![image](https://github.com/user-attachments/assets/e9797bf6-57fb-422a-ac19-42de36637170)








## RESULT
Thus the program to perform the basic left shift operation for 44 integer number with 3 shifts has been executed successfully.




 
 


# EX-17-TWO-NUMBERS-ARE-EQUAL-OR-NOT


## AIM

Write a C Program to check whether the two numbers are equal or not using simple if statement.

## ALGORITHM

1.	Start the program.
2.	Read two numbers.
3.	If first number is equal to second number, display both are equal.
4.	Otherwise display both are not equal.
5.	Stop the program.

## PROGRAM
``` c
#include <stdio.h>

int main() {
    int num1, num2;

    printf("Enter the first number: ");
    scanf("%d", &num1);
    printf("Enter the second number: ");
    scanf("%d", &num2);

    if (num1 == num2) {
        printf("Both numbers are equal.\n");
    } else {
        printf("Both numbers are not equal.\n");
    }

    return 0;
}

```

## OUTPUT
### Values are not equal
![image](https://github.com/user-attachments/assets/c79f7c3a-2f60-4d72-8a5d-96c57697c331)
  
### Values are equal
![image](https://github.com/user-attachments/assets/269ada18-474f-409d-b030-ec41222b144e)

## RESULT

Thus the program to check whether the two numbers are equal or not using simple if statement has been executed successfully
 
 


# EX-18-STRING-LOWERCASE-CONVERSION
## AIM
Write a C Program to convert the given string into lowercase.

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Using tolower( ) function convert the given string into its lowercase.
4.	Display the result.
5.	Stop the program.

## PROGRAM
```c
#include <stdio.h>
#include <ctype.h> 

int main() {
    char str[100];
    int i;

    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin); 

    for (i = 0; str[i] != '\0'; i++) {
        str[i] = tolower(str[i]); 
    }

    printf("The lowercase string is: %s", str);

    return 0;
}

```
## OUTPUT
![image](https://github.com/user-attachments/assets/5b257532-8aa5-4672-b9f9-18235068bc7c)




## RESULT
Thus the program to convert the given string into lowercase has been executed successfully
 
 


# EX-19-COUNT-OF-WORDS-IN-A-STRING
## AIM
Write a C Program to count the total number of words in a given string using do While loop.

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Using for loop, inspect the string character by character.
4.	Whenever a space is encountered increment count by 1.
5.	Display the result.
6.	Stop the program.

## PROGRAM
``` c
#include <stdio.h>
#include <string.h>

int main() {
    char str[100];
    int i = 0, wordCount = 0;

    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);

    str[strcspn(str, "\n")] = '\0';

    if (str[0] != ' ' && str[0] != '\0') {
        wordCount = 1; 
    }

    do {
        if (str[i] == ' ' && str[i + 1] != ' ' && str[i + 1] != '\0') {
            wordCount++;
        }
        i++;
    } while (str[i] != '\0');

    printf("The total number of words in the string is: %d\n", wordCount);

    return 0;
}

```
## OUTPUT
![image](https://github.com/user-attachments/assets/043ed5e8-e81b-4252-b5ef-d303d2f03352)





## RESULT
Thus the program to count the total number of words in a given string using do While loop has been executed successfully
 
 


# EX  -20 -COMPARING TWO STRINGS
## AIM
write a Program to compare two strings without using strcmp().
## ALGORITHM
### Step 1: 
Start the program.

### Step 2: 
Declare two character arrays c1 and c2 of size 100 to store the strings. Also, declare an integer variable
flag and initialize it to 0, and i for indexing.      

### Step 3: 
Read the first string c1 using scanf("%[^\n]", c1); — this reads input until a newline is encountered 
i.e., can include spaces).

### Step 4: 
Read the second string c2 using scanf("%s", c2); — this reads input until a space or newline (i.e., no 
spaces in the second string).

### Step 5: 
Start comparing characters of both strings from index i = 0.

### Step 6: 
Repeat the following while neither c1[i] nor c2[i] is '\0' (i.e., end of string):

•	If c1[i] is not equal to c2[i], set flag = 1.

•	Increment i by 1.

### Step 7: 
After the loop, check the value of flag:

•	If flag == 0, print "strings are same".

•	Otherwise, print "strings are not same".

### Step 8: 
End the program.

## PROGRAM
``` c
#include <stdio.h>

int main() {
    char c1[100], c2[100];
    int i = 0, flag = 0;

    printf("Enter the first string: ");
    scanf("%[^\n]", c1); 

    getchar(); 
    printf("Enter the second string: ");
    scanf("%s", c2); 

    while (c1[i] != '\0' && c2[i] != '\0') {
        if (c1[i] != c2[i]) {
            flag = 1; 
            break;
        }
        i++;
    }

    if (c1[i] != '\0' || c2[i] != '\0') {
        flag = 1;
    }

    if (flag == 0) {
        printf("Strings are the same.\n");
    } else {
        printf("Strings are not the same.\n");
    }

    return 0;
}

```

## OUTPUT
 ### Strings are same
 ![image](https://github.com/user-attachments/assets/6fa73289-1ed8-4150-90ee-76180a52b746)

 ### Strings are not same
 ![image](https://github.com/user-attachments/assets/120db32d-76b3-4717-8fe3-1ee6d853a8f2)


## RESULT
Thus the C Program to compare two strings without using strcmp() has been executed successfully.

