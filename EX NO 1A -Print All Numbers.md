
# EX 1A Print All Numbers 
## DATE:22-01-2026

## AIM:
To Write a Java program that takes an integer input N from the user and prints all the numbers from 1 to N, separated by spaces, on a single line..

## Algorithm

1. Start the program and import the Scanner class to take user input.
2. Create a Scanner object to read an integer input N from the user.
3.Check if N is greater than 0; if not, display "Invalid input. N must be greater than    0."
4.Use a for loop to iterate from 1 to N.
5.Print each number separated by a space on the same line.
  

## Program:
```
/*
Program to implement Reverse a String
Developed by: Naveenkumar M
Register Number:  212224230182
*/
```
```
import java.util.Scanner;

public class Numprint
{
    public static void main(String[] args)
    {
        Scanner n= new Scanner(System.in);
        int num=n.nextInt();
        
        for(int i=1;i<=num;i++)
        {
            System.out.print(i+" ");
        }
    }
}
```

## Output:

<img width="440" height="161" alt="image" src="https://github.com/user-attachments/assets/bd3ae338-bf69-4ad2-a844-08d38e0e6741" />


## Result:
The program successfully print all the numbers from 1 to N. 
