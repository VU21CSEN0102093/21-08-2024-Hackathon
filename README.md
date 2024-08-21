# 21-08-2024-Hackathon

import java.util.Scanner;

public class ThreeLevelPasswordSystem {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Step 1: Textual Password
        String correctPassword = "password123";
        System.out.print("Enter your textual password: ");
        String inputPassword = scanner.nextLine();

        if (!inputPassword.equals(correctPassword)) {
            System.out.println("Authentication Failed: Incorrect textual password.");
            return;
        }

        // Step 2: PIN Code
        int correctPin = 4321;
        System.out.print("Enter your 4-digit PIN code: ");
        int inputPin = scanner.nextInt();

        if (inputPin != correctPin) {
            System.out.println("Authentication Failed: Incorrect PIN code.");
            return;
        }

        // Step 3: Security Question
        String correctAnswer = "blue";
        scanner.nextLine();  // Consume newline left-over
        System.out.print("What is your favorite color? ");
        String inputAnswer = scanner.nextLine();

        if (!inputAnswer.equalsIgnoreCase(correctAnswer)) {
            System.out.println("Authentication Failed: Incorrect answer to security question.");
            return;
        }

        // If all three checks pass
        System.out.println("Authentication Successful: Access Granted.");
    }
}

