import java.util.*;
import java.util.random.*;
public class num_game {
    public static void main(String[] args) {
        Random r1 = new Random();
        int r1_int1 = r1.nextInt(100); 
        Scanner sc = new Scanner(System.in);
        System.out.println(" the number of passes are 3");
        int passes = 3;
        int i;
        for(i=0;i<passes;i++){
            System.out.println(
				"Guess the number:");

			// Take input for guessing
			 int guess = sc.nextInt();

			// If the number is guessed
			if (r1_int1 == guess) {
				System.out.println(
					"Congratulations!"
					+ " You guessed the number.");
				break;
			}
			else if (r1_int1 > guess
					&& i != passes - 1) {
				System.out.println(
					"The number is "
					+ "greater than " + guess);
			}
			else if (r1_int1 < guess
			&& i != passes - 1) {
				System.out.println(
					"The number is"
					+ " less than " + guess);
			}
		}

		if (i == passes) {
			System.out.println(
				"You have exhausted the numner of passes ");

			System.out.println( "The random genrated number was " + r1_int1);
		}
	
    
    }}

