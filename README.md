/* An ISBN-10 (International Standard Book Number)
consists of 10 digits: d1d2d3d4d5d6d7d8d9d10. The last digit, d10, is a checksum,
which is calculated from the other nine digits using the following formul:
(d1 * 1 + d2 * 2 + d3 * 3 + d4 * 4 + d5 * 5 +
d6 * 6 + d7 * 7 + d8 * 8 + d9 * 9) % 11 /*

# Extra_Ex3_7

package com.personal.ExtraEx3_7;

import java.util.Arrays;
import java.util.Scanner;

public class Extra3_7 {

	public static void main(String[] args) {

		System.out.println("****** Calculating the # 10 of ISBN");

		Scanner sc= new Scanner(System.in);
		String isbn;
		double sum=0;
		System.out.println("Enter the nine number of ISBN");
		isbn=sc.next();
		char[] digit= isbn.toCharArray();
		
		for (int i = 0; i < digit.length; i++) {

			//sum +=(int)digit[i]-48;
	    	sum += ((((int)digit[i]-48))*(i+1));
	    	//System.out.println(digit[i]);
		
		}
		System.out.println("the #10 of ISBN is :" + Math.round(sum *(11/100) ));

		
		
	
}}
