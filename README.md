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

## Step 7:

Store the sums of the diceRoll and the user's inputs into their respective variables. Then print out the results in the form of a sentence:

```java
        int sumOfNumbers = num1 + num2 + num3;
        int sumOfRolls = roll1 + roll2 + roll3;
        System.out.println("Dice sum = " + sumOfRolls + ". Your number sum = " + sumOfNumbers);
```

## Step 8:

Create the checkWin() function to see who wins:

```java
public static boolean checkWin(int sumOfRolls, int sumOfNumbers) {
        return (sumOfNumbers > sumOfRolls && (sumOfNumbers - sumOfRolls) < 3);  
    }
```

## Step 9:

Write an if-else statement to display to the user whether they won or lost:

```java
        if (checkWin(sumOfRolls, sumOfNumbers)) {
            System.out.println("Congrats! You win!");
        } else {
            System.out.println("Sorry! You lose!");
        }
```