// My little project
// in java

// The pseudocode
import java.util.Scanner;
// The interface
interface Business {
  // The methods
  public void Intro();
  public void clerk();
}
// The first but not main class and implemented interface
class Buss implements Business {
  public void Intro() {
	  // THE Welcome
        System.out.println("        Welcome to Snovz!       ");
        System.out.println("  This is an Electronic Repair Shop. ");
  }
  public void clerk() {
    	  System.out.println("        How may I help you?        ");
        System.out.println("-----------------------------------------------------------");
        System.out.println("         THE ITEMS WE FIX         ");
        System.out.println("         For Big Items is 1         ");
        System.out.println("         For Medium Items is 2         ");
        System.out.println("         For Small Items is 3         ");
	  System.out.println("	 To QUIT is Above 3 or any key letter	");
	  // Your Reply 
        System.out.println("	 Enter Your Option		");
  }
}

class BisDemo {
    public static void main(String[] args) {
	  for(int i = 0; i < 10; i++) { // Somewhat of infinite loop
        // variable that I use
	  double Amount = 58.00;
        double Change1, Change2, Change3;
        double Big = 43.50, Medium = 25.40, Small = 13.00;
        Change1 = Amount - Big;
        Change2 = Amount - Medium;
        Change3 = Amount - Small;
	  // The amount of money you "Have"
        System.out.println("    The Amount of Money in Your Wallet is:  " + "$" + Amount);
	  
	  Buss myIntro = new Buss();
	  myIntro.Intro();

	  Buss myclerk = new Buss();
	  myclerk.clerk();

	  // The option(s) You're going to choose
        Scanner sc = new Scanner(System.in);
        int option = sc.nextInt();

        switch (option) { // The switch case
            case 1:
                // 2ND RESPONSE
                System.out.println("    BIG ITEMS     ");
                System.out.println("                ");
                System.out.println("  Refrigerators, Ovens, Dryers  ");
		    System.out.print("	Your change is: " + "$" + Change1 + " ");
                break;
            case 2:
                // 3RD RESPONSE
                System.out.println("    MEDIUM ITEMS  ");
                System.out.println("		    ");
                System.out.println("  Game Consoles, TVs, PCs  ");
		    System.out.print("	Your change is: " + "$" + Change2 + " ");
                break;
            case 3:
                System.out.println("    SMALL ITEMS   ");
                System.out.println("		    ");
                System.out.println("  Microwaves, Drones, External Hardware ");
		    System.out.print("	Your change is: " + "$" + Change3 + " ");
                break;
            default:
                System.out.println("-----------------------------------------------------------");
                System.out.println("Thank You For Checking This Program Out!");
                System.out.println("-----------------------------------------------------------");
      }  // The switch case
    } // infinite loop  
  }
}
