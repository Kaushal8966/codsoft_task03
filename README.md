# codsoft_task03
#currency calculator
import java.util.Scanner;

public class CurrencyConverter {
    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Welcome to currency converter");
        System.out.println("1. USD to Rupee");
        System.out.println("2. Rupee to USD");
        System.out.println("3. Euro to Rupee");
        System.out.println("4. Rupee to Euro");
        int choice = sc.nextInt();
        
        if (choice == 1) {
            System.out.println("Enter the amount in USD:");
            double USD = sc.nextDouble();
            double RUPEE = usdToRupee(USD);
            System.out.println("Amount converted in Rupee: " + RUPEE);
        } else if (choice == 2) {
            System.out.println("Enter the amount in Rupee:");
            double RUPEE = sc.nextDouble();
            double USD = rupeeToUsd(RUPEE);
            System.out.println("Amount converted in USD: " + USD);
        } else if (choice == 3) {
            System.out.println("Enter the amount in Euro:");
            double EURO = sc.nextDouble();
            double RUPEE = euroToRupee(EURO);
            System.out.println("Amount converted in Rupee: " + RUPEE);
        } else if (choice == 4) {
            System.out.println("Enter the amount in Rupee:");
            double RUPEE = sc.nextDouble();
            double EURO = rupeeToEuro(RUPEE);
            System.out.println("Amount converted in Euro: " + EURO);
        } else {
            System.out.println("INVALID CHOICE! Please select 1, 2, 3, or 4.");
        }
        
        sc.close();
    }

    public static double usdToRupee(double USD) {
        return USD * 83.47;
    }

    public static double rupeeToUsd(double RUPEE) {
        return RUPEE * 0.0119004;
    }

    public static double euroToRupee(double EURO) {
        return EURO * 89.10;
    }

    public static double rupeeToEuro(double RUPEE) {
        return RUPEE * 0.01122; // Corrected the conversion rate
    }
}
