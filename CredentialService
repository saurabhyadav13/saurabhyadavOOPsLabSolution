package com.xyz.driver;

import java.util.Random;


public class CredentialService {
	private String emailAddress;
	private String password;
	private Employee lEmployee;

	public CredentialService(Employee pEmployee) {
		this.lEmployee = pEmployee;
		this.generatePassword();
		this.generateEmailAddress();
		this.showCredentials();
	}

	private String getEmailAddress() {
		return emailAddress;
	}

	private void setEmailAddress(String emailAddress) {
		this.emailAddress = emailAddress;
	}

	private String getPassword() {
		return password;
	}

	private void setPassword(String password) {
		this.password = password;
	}

	private void generatePassword() {
		int lLength = 8;
		String lUpperCaseLetters = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
		String lLowerCaseLetters = "abcdefghijklmnopqrstuvwxyz";
		String lSpecialCharacters = "!@#$";
		String lNumbers = "1234567890";
		String lCombinedChars = lUpperCaseLetters + lLowerCaseLetters + lSpecialCharacters + lNumbers;
		Random lRandom = new Random();
		char[] lPassword = new char[lLength];

		lPassword[0] = lUpperCaseLetters.charAt(lRandom.nextInt(lUpperCaseLetters.length()));
		lPassword[1] = lLowerCaseLetters.charAt(lRandom.nextInt(lLowerCaseLetters.length()));
		lPassword[2] = lSpecialCharacters.charAt(lRandom.nextInt(lSpecialCharacters.length()));
		lPassword[3] = lNumbers.charAt(lRandom.nextInt(lNumbers.length()));

		for (int i = 4; i < lLength; i++) {
			lPassword[i] = lCombinedChars.charAt(lRandom.nextInt(lCombinedChars.length()));
		}
		this.setPassword(String.valueOf(lPassword));
	}

	private void generateEmailAddress() {
		String lEmail = lEmployee.getFirstName() + lEmployee.getLastName() + "@" + lEmployee.getDepartmentName() + "."
				+ lEmployee.getCompanyName() + ".com";
		this.setEmailAddress(lEmail.toLowerCase());
	}

	private void showCredentials() {
		System.out.println("Dear " + lEmployee.getFirstName() + " your generated credentials are as follows");
		System.out.println("Email --> " + this.getEmailAddress());
		System.out.println("Password --> " + this.getPassword());
	}
}
