# MBI-Computation-Java
This is a Program computing the Mass Body Index based on weight in Kgs and height in meters.

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

// prompt the users inputting height and weight;
        System.out.print("Enter weight in Kg: ");
        double weightInKg = input.nextDouble();
        System.out.print("Enter height in meter: ");
        double heightInMeters = input.nextDouble();

        double mbi = weightInKg / (heightInMeters * heightInMeters);

        System.out.println("Your MBI is " + mbi);

        if (mbi < 18.5)
            System.out.println("You are underweight based on your MBI.");
        else if(mbi < 25.0)
            System.out.println("You have normal weight based on your MBI.");
        else if(mbi < 30.0)
            System.out.println("You have overweight based on your MBI.");
        else
            System.out.println("You are obese based on your MBI.");
    }
}
