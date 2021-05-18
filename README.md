# Weightliftinghelper
This program allows you to enter your maximum lift weight for benchpress, squat, and deadlift, provide a projected goal for weekly weight to add to your lift, and also calculates percentages of your max.
package weightlifting.program;

import java.util.Scanner;

public class LiftingMainClass {

	//Declare local constants
	final static double WEEKLY_INCREASE_BENCH = .02083;
	final static double WEEKLY_INCREASE_SQUAT = .05416;
	final static double WEEKLY_INCREASE_DEADLIFT = .06666;
	
	//main method
	public static void main(String[] args)
	{
	
	//declare and initialize scanner
	Scanner input = new Scanner(System.in);
	
	//declare all local variables
	double benchMax = 0.0;
	double squatMax = 0.0;
	double deadliftMax = 0.0;
	double preferredPercentage = 0.0;
	double weeklybenchIncrease = 0.0;
	double weeklysquatIncrease = 0.0;
	double weeklydeadliftIncrease = 0.0;
	double updatedBench = 0.0;
	double updatedSquat = 0.0;
	double updatedDeadlift = 0.0;
	double percentbenchMax = 0;
	double percentsquatMax = 0;
	double percentdeadliftMax = 0;
	
	//display welcome banner
	System.out.println("Weightlifting Percentages Calculator");
	System.out.println("Enter the following");
	
	//input
	//input for bench max
	System.out.println("Bench Press Max:");
	//assignment statement
	benchMax = input.nextDouble();
	
	//input for squat max
	System.out.println("Squat Max:");
	//assignment statement
	squatMax = input.nextDouble();
	
	//input for deadlift max
	System.out.println("Deadlift Max:");
	//assignment statement
	deadliftMax = input.nextDouble();
	
	//input for percentage
	System.out.println("Preferred Percentage:");
	//assignment statement
	preferredPercentage = input.nextDouble();
	
	//process section
	
	//assignment statement, weekly bench increase
	weeklybenchIncrease = benchMax * WEEKLY_INCREASE_BENCH;
	
	//assignment statement, updated bench weight
	updatedBench = weeklybenchIncrease + benchMax;
	
	//assignment statement, weekly squat increase
	weeklysquatIncrease = squatMax * WEEKLY_INCREASE_SQUAT;
	
	//assignment statement, updated squat weight
	updatedSquat = weeklysquatIncrease + squatMax;
			
	//assignment statement, weekly deadlift increase
	weeklydeadliftIncrease = deadliftMax * WEEKLY_INCREASE_DEADLIFT;
	
	//assignment statement, updated deadlift weight
	updatedDeadlift = weeklydeadliftIncrease + deadliftMax;
	
	//assignment statement
	percentbenchMax = benchMax * preferredPercentage/100;
			
	//assignment statement
	percentsquatMax = squatMax * preferredPercentage/100;
	
	//assignment statement
	percentdeadliftMax = deadliftMax * preferredPercentage/100;
	
	
	
	//output
	
	System.out.println("------------------------------------------------------------------");
	System.out.printf("%-20s%.1f%s\n", "Weekly Bench Increase: ", weeklybenchIncrease, " lbs.");
	
	System.out.printf("%-20s%.1f%s\n", "Weekly Squat Increase: ", weeklysquatIncrease, " lbs.");
	
	System.out.printf("%-20s%.1f%s\n\n", "Weekly Deadlift Increase: ", weeklydeadliftIncrease, " lbs.");
	
	
	System.out.printf("%-20s%.1f%s\n", "Next Week Bench Goal Weight: ", updatedBench, " lbs.");
	
	System.out.printf("%-20s%.1f%s\n", "Next Week Squat Goal Weight: ", updatedSquat, "lbs.");
	
	System.out.printf("%-20s%.1f%s\n", "Next Week Deadlift Goal Weight: ", updatedDeadlift, " lbs."); 
	System.out.println("------------------------------------------------------------------");
	System.out.printf("%-5s%3s%3s%.1f%s\n", preferredPercentage, " % ", "of Bench Press Max: ", percentbenchMax, " lbs.");
	
	System.out.printf("%-5s%3s%3s%.1f%s\n", preferredPercentage, " % ", "of Squat Max: ", percentsquatMax, " lbs.");
	
	System.out.printf("%-5s%3s%3s%.1f%s\n", preferredPercentage, " % ", "of Deadlift Max: ", percentdeadliftMax, " lbs.");
	System.out.println("------------------------------------------------------------------");
	
	//display farewell message
	System.out.println("Thanks for using!");
	
	//close scanner
	input.close();
	
	}//end of main method
	
}//end main class
