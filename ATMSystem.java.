
import java.util.Scanner;

public class ATMSystem {

    public static void main(String[] args) {

        Scanner input = new Scanner(System.in);

        double balance = 5000.00;
        double amount;
        int choice;
        char again = 'Y';

        System.out.println("Welcome to the ATM Banking System!");

        while (again == 'Y' || again == 'y') {

            System.out.println("\n===== ATM MENU =====");
            System.out.println("1. Check Balance");
            System.out.println("2. Deposit Money");
            System.out.println("3. Withdraw Money");
            System.out.println("4. Exit");
            System.out.print("Choose an option: ");

            choice = input.nextInt();

            if (choice == 1) {

                System.out.printf(
                    "Current Balance: PHP %.2f%n", balance
                );

            } else if (choice == 2) {

                System.out.print("Enter deposit amount: PHP ");
                amount = input.nextDouble();

                if (amount > 0) {
                    balance += amount;

                    System.out.printf(
                        "Deposit successful!%nNew Balance: PHP %.2f%n",
                        balance
                    );
                } else {
                    System.out.println(
                        "Invalid amount! Deposit must be positive."
                    );
                }

            } else if (choice == 3) {

                System.out.print("Enter withdrawal amount: PHP ");
                amount = input.nextDouble();

                if (amount <= 0) {
                    System.out.println("Invalid withdrawal amount!");
                } else if (amount > balance) {
                    System.out.println("Insufficient balance!");
                } else {
                    balance -= amount;

                    System.out.printf(
                        "Withdrawal successful!%nNew Balance: PHP %.2f%n",
                        balance
                    );
                }

            } else if (choice == 4) {

                System.out.println("Thank you for using our ATM!");
                break;

            } else {

                System.out.println(
                    "Invalid choice! Please select 1 to 4."
                );
            }

            System.out.print(
                "Would you like another transaction? (Y/N): "
            );
            again = input.next().charAt(0);
        }

        System.out.println("ATM session ended.");

        input.close();
    }
}
