# DiceJack_Java
Create an interactive dice game using Java. The user can input 3 values, which will be summed. The machine will roll the dice 3 times. If the user's sum is greater than the sum of the rolls, and the difference is less than 3, the user wins. Otherwise, the machine wins.

## Step 1: 

Import **Scanner**:

```java
import java.util.Scanner;
```

## Step 2:

Create the DiceJack class:

```java
public class DiceJack {
    public static void main(String[] args) {
    }
```

## Step 3:

Instantiate the new **Scanner** instance:

```java
Scanner scan = new Scanner(System.in);
```

## Step 4:

Create and call the rollDice() function:

```java
public static int rollDice() {
        double randomNumber = Math.random() * 6;
        randomNumber += 1;
        return (int)randomNumber;
    }

        int roll1 = rollDice();
        int roll2 = rollDice();
        int roll3 = rollDice();
```

## Sep 5: 

Ask the user to enter 3 values between 1 and 6. Then use **Scanner** to receive their input:

```java
System.out.println("Enter 3 numbers between 1 and 6");
        int num1 = scan.nextInt();
        int num2 = scan.nextInt();
        int num3 = scan.nextInt();
```

## Step 6:

Write 2 if-statements to verify that the numbers entered by the user are between 1-6. If any number does not meet these requirements, we shut down the program:

```java
        if (num1 < 1 || num2 < 1 || num3 < 1) {
            System.out.println("Numbers cannot be less than 1. Shutting the game down!");
            System.exit(0);
        }
        if (num1 > 6 || num2 > 6 || num3 > 6) {
            System.out.println("Numbers cannot be greater than 6. Shutting game down!");
            System.exit(0);
        }
```