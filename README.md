# ATM_program
import java.util.*;


public class ATM_Progaram
{
			double amount=100000.00;
			String name="MR. K.N.U.Ranasinghe";
			String ac="1702121354545446";
			String id="200045455207";
			int choise;
			double newprice;
			
			double price;
			double price1;
			
			
	
	public static void main (String []args)
	{
			
			int choise;
			double newprice;
			
			Scanner inputs =new Scanner(System.in);
			

			
		while(true)
		{
			System.out.println("\t\t\t[[<<--AUTOMATIC TELLER SYSTEM-->>]] \n\n ");
			System.out.println("Enter your choice \n 1-withdraw \n 2-diposit \n 3-Account details \n 4-Exit");
			
			choise = inputs.nextInt();
			
			ATM_Progaram ob = new ATM_Progaram();
			
		
			
			if(choise == 1) {
				
				System.out.println("Enter your withdraw ammount : ");
			newprice = inputs.nextDouble();
			ob.withdraw(newprice);
				
			}
			else if(choise == 2){
			
			System.out.println("Enter your diposit ammount : ");
			newprice = inputs.nextDouble();
			ob.diposit(newprice);
				
			}
			else if(choise == 3) {
				ob.inquary();
			}
			else {
				ob.exit();
			}
		}
			
	}
	
	 public void withdraw (double x){
			price = amount - x;
			System.out.print("Balance : "+price);
			System.out.print(" " );
		}
		
	public void diposit(double x){
			price1 = amount + x;
			System.out.print("Balance : "+price1);
			System.out.print(" " );
	}
	public void inquary(){
			
			System.out.println("Account balance : "+amount);
			System.out.println("Account Name : "+name);
			System.out.println("ID number : "+id);
			System.out.println("Account Number : "+ac);
			System.out.print(" " );
			
	}
	public void exit(){
			 System.exit(0);  
	}
	
	
}
