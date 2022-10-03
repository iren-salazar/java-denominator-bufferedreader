# java-denominator-bufferedreader
denominator is a modulo. this prog. lets you input multiple nums and ask you if you want to inpput over and over again intil you decise to say no it will stop you from inputting nums and prints the denominators....


package mates;

import java.io.*;

public class Denominatorkent {
	public static void main(String args[]) throws Exception {
		
		BufferedReader br = new BufferedReader (new InputStreamReader(System.in));
		
		int money, onethou = 0, fivehun = 0, twohun = 0, onehun = 0, fifty = 0, tweny = 0, ten = 0;
		String choice;
		
		System.out.println("DENOMINATION: ");
		
		do {
			System.out.println("Input an amount: ");
			money = Integer.parseInt(br.readLine());
			
			switch (money) {
			
			case 1000:
			onethou++;
			break;
			
			case 500:
			fivehun++;
			break;
			
			case 200:
			twohun++;
			break;
			
			case 100:
			onehun++;
			break;
			
			case 50:
			fifty++;
			break;
			
			case 20:
			tweny++;
			break;
			
			case 10:
			ten++;
			break;
			}
			
			System.out.println("Do you want to input money again (Y/N)?: ");
			
			choice = br.readLine().toUpperCase();
			
			switch (choice) {
			
			case "N":
				System.out.println("1000: " + onethou);
				System.out.println("500: " + fivehun);
				System.out.println("200: " + twohun);
				System.out.println("100: " + onehun);
				System.out.println("50: " + fifty);
				System.out.println("20: " + tweny);
				System.out.println("10: " + ten);
				
				break;
				}
		} while(choice.equals("Y"));
	}

}
