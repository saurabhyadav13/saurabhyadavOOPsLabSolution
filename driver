package com.xyz.driver;

import java.util.Scanner;


public class Driver {

	public static void main(String[] args) {

		if (args.length != 3 && args.length != 0) {
			System.out.println("Please enter valid arguments i.e. 3 (FisrtName LastName CompanyName) OR  0 (Leave empty for user input)");
			return;
		}
		String lEmployeeFirstName = null;
		String lEmployeeLastName = null;
		String lCompanyName = null;

		Scanner lScanner = new Scanner(System.in);

		if (args.length == 0) {
			System.out.println("Please enter first name for employee: ");
			lEmployeeFirstName = lScanner.nextLine();
			System.out.println("Please enter last name for employee: ");
			lEmployeeLastName = lScanner.nextLine();
			System.out.println("Please enter company name for employee: ");
			lCompanyName = lScanner.nextLine();
		} else {
			lEmployeeFirstName = args[0];
			lEmployeeLastName = args[1];
			lCompanyName = args[2];
		}

		Employee lEmployee = new Employee(lEmployeeFirstName, lEmployeeLastName);
		lEmployee.setCompanyName(lCompanyName);

		int lChoice = 0;

		do {
			System.out.print("Please enter the department from the following \n" + "1. Technical \n" + "2. Admin \n"
					+ "3. Human Resource \n" + "4. Legal \n");

			lChoice = Integer.valueOf(lScanner.nextLine());

			switch (lChoice) {

			case 1: {

				lEmployee.setDepartmentName("Tech");

			}

				break;

			case 2: {

				lEmployee.setDepartmentName("Admin");

			}

				break;

			case 3: {

				lEmployee.setDepartmentName("HR");

			}

				break;

			case 4: {

				lEmployee.setDepartmentName("Legal");

			}

				break;

			default:

				System.out.println("Invalid choice. Enter a valid no.");

			}

		} while (lChoice < 1 || lChoice > 4);

		new CredentialService(lEmployee);

		lScanner.close();
	}
}
