Air Ticket Price Calculation

import java.util.Scanner;

public class Odev14 {
    public static void main(String[] args) {

        int distance,age,tripType;
        double mainAmount = 0;



        Scanner input = new Scanner(System.in);
        System.out.println("Enter the distance in km :");
        distance = input.nextInt();


        System.out.println("Enter your age: ");
        age = input.nextInt();

        System.out.println("Choose your trip type :");
        System.out.println("Press 1 for one-way.");
        System.out.println("Press 2 for round trip.");
        tripType = input.nextInt();

        if((age < 0 || distance < 0 || tripType < 1 || tripType > 2)) {
            System.out.println("Incorrect Entry !");
        }
        else {
            mainAmount = distance * 0.10;
            if (age < 12) {
                mainAmount = mainAmount / 2;

            } else if ((age > 11) && (age < 25)) {
                mainAmount = mainAmount / 10;

            } else if (age > 65) {
                mainAmount = mainAmount * 3 /10;
            }
            else{
                mainAmount = mainAmount;            }
        }
        if (tripType == 1){
            System.out.println("Your type of trip : One Direction " );
            System.out.println("Amount :" + mainAmount * 10 + " TL" );
        if(tripType ==2){
                System.out.println("Your type of trip : Round Trip");
                System.out.println("Amount :" + ( mainAmount /5) + " TL" );
            }
        else {
                System.out.println("Incorrect Entry !" );
            }
        }

    }

}
