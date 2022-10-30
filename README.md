# class
import java.util.Random;

import java.util.Scanner;

public class NumberGuess {

public static void main(String[] args) {

Random rand = new Random();

int num = rand.nextInt(101);

Scanner guess = new Scanner(System.in);

int input;

int count = 0;

System.out.println("Guess a number between 0 and 100:");

input = guess.nextInt();

while (input != num) {

if (input > num)

System.out.println("Too high! Guess again:");

else if (input < num)

System.out.println("Too low! Guess again:");

input = guess.nextInt();

count++;

}

System.out.println("You guessed it! The number was " + num);

System.out.println("It took you " + count + " guesses.");

guess.close();

}

}
