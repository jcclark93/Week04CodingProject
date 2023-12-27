"# Week04CodingProject" 
"# Week04CodingProject" 
package week4CodingProject;

import java.util.Arrays;

public class Week04CodingProject {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		
		
		//1. Create an array of int called ages that contains the following values: 3, 9, 23, 64, 2, 8, 28, 93.
		int[] ages = {3, 9, 23, 64, 2, 8, 28, 93};

		//a. Programmatically subtract the value of the first element in the array from the value in the last element of the array (i.e. do not use ages[7] in your code). Print the result to the console.  
		int ageValue = ages[ages.length -1] - ages[0];
		System.out.println(ageValue);
		
		//b. Create a new array of int called ages2 with 9 elements (ages2 will be longer than the ages array, and have more elements).  
		int[] ages2 = {17, 2, 13, 16, 12, 29, 70, 82, 56};
		
		//i. Make sure that there are 9 elements of type int in this new array.  
		int ages2length = ages2.length;
		System.out.println("Question 1.i: " + ages2length);
		//ii. Repeat the subtraction from Step 1.a. (Programmatically subtract the value of the first element in the new array ages2 from the last element of ages2). 
		int age2Value = ages2[ages2.length -1] - ages2[0];
		System.out.println("Question 1.ii: " + age2Value);
		//iii. Show that using the index values for the elements is dynamic (works for arrays of different lengths).
		int[] ages3 = {13, 22, 27};
		int age3Value = ages3[ages3.length -1] - ages3[0];
		System.out.println("Question 1.iii:" + age3Value);
		
		//c. Use a loop to iterate through the array and calculate the average age. Print the result to the console.
		int sum = 0;
		for (int i =0; i < ages2.length; i++) {
			sum += ages2[i];
		} System.out.println(sum/ages2.length);
		
		//2. Create an array of String called names that contains the following values: “Sam”, “Tommy”, “Tim”, “Sally”, “Buck”, “Bob”.
		String[] names = {"Sam", "Tommy", "Tim", "Sally", "Buck", "Bob"};
		
		//a. Use a loop to iterate through the array and calculate the average number of letters per name. Print the result to the console.
		int sumLetters = 0;
		for (String name: names) {
			sumLetters += name.length();
		} int avgLetters = sumLetters/names.length;
		System.out.println(avgLetters);
		//b. Use a loop to iterate through the array again and concatenate all the names together, separated by spaces, and print the result to the console.
		StringBuilder sb = new StringBuilder();
		String space = " ";
		for (String name : names) {
			sb.append(name);
			sb.append(space);
		} String concatName = sb.toString();
		System.out.println(concatName);
		//3. How do you access the last element of any array?
		// array[array.length -1];

		//4. How do you access the first element of any array?
		//array[0];

		//5. Create a new array of int called nameLengths. Write a loop to iterate over the previously created names array and add the length of each name to the nameLengths array.
		int[] nameLengths = new int[names.length];
		for (int i = 0; i < names.length; i++) {
			nameLengths[i] += names[i].length();
		} System.out.println(Arrays.toString(nameLengths));
		
		
		//6. Write a loop to iterate over the nameLengths array and calculate the sum of all the elements in the array. Print the result to the console.
		int sumNameLengths = 0;
		for (int length: nameLengths) {
			sumNameLengths += length;
		} System.out.println(sumNameLengths); 
		
		//7. Write a method that takes a String, word, and an int, n, as arguments and returns the word concatenated to itself n number of times. (i.e. if I pass in “Hello” and 3, I expect the method to return “HelloHelloHello”). 
		String tripleHello = concatenateWord ("Hello", 5);
		System.out.println(tripleHello);
	
		//8. Write a method that takes two Strings, firstName and lastName, and returns a full name (the full name should be the first and the last name as a String separated by a space).
		String fullName = getFullName ("Jessica", "Clark");
		System.out.println(fullName);
		
		//9. Write a method that takes an array of int and returns true if the sum of all the ints in the array is greater than 100.
		boolean result9 = isSumGreater100 (ages2);
		System.out.println(result9);
		
		//10. Write a method that takes an array of double and returns the average of all the elements in the array.
		double[] array10 = {10.4, 17.7, 19.3};
		double result10 = getAverageElements (array10);
		System.out.println(result10);
		
		//11. Write a method that takes two arrays of double and returns true if the average of the elements in the first array is greater than the average of the elements in the second array.
		double firstArray[] = {7.2, 9.8, 17.4, 12.9, 13.5};
		double secondArray[] = {4.5, 7.9, 20.3, 14.7, 3.9};
		System.out.println(getHigherAvg(firstArray, secondArray));
		//12. Write a method called willBuyDrink that takes a boolean isHotOutside, and a double moneyInPocket, and returns true if it is hot outside and if moneyInPocket is greater than 10.50.
		boolean isHotOutside = true;
		double moneyInPocket = 13.50;
		System.out.println(willBuyDrink(isHotOutside, moneyInPocket));
		//13. Create a method of your own that solves a problem. In comments, write what the method does and why you created it.
		boolean haveAYard = true;
		int savingsAccount = 4500;
		System.out.println(canHavePuppy(haveAYard, savingsAccount));
	}//end of main
	//7. Write a method that takes a String, word, and an int, n, as arguments and returns the word concatenated to itself n number of times. (i.e. if I pass in “Hello” and 3, I expect the method to return “HelloHelloHello”).
	public static String concatenateWord(String word, int n) {
		StringBuilder result = new StringBuilder();
		for (int i = 0; i < n; i++) {
			result.append(word);
		} return result.toString();
	}
	//8. Write a method that takes two Strings, firstName and lastName, and returns a full name (the full name should be the first and the last name as a String separated by a space).
	public static String getFullName(String firstName, String lastName) {
		return firstName + " " + lastName;
	}
	//9. Write a method that takes an array of int and returns true if the sum of all the ints in the array is greater than 100.
	public static boolean isSumGreater100(int[] array) {
		int sumGr = 0;
		for (int arr: array) {
			sumGr += arr;
		} return sumGr > 100;
	}
	//10. Write a method that takes an array of double and returns the average of all the elements in the array.
	public static double getAverageElements(double[] array) {
		double sumAvg = 0;
		for (double avg : array) {
			sumAvg += avg;
		} return sumAvg / array.length;
	}
	

	//11. Write a method that takes two arrays of double and returns true if the average of the elements in the first array is greater than the average of the elements in the second array.
	public static boolean getHigherAvg(double firstArray[], double secondArray[]) {
		double sumAverage1 = 0;
		double sumAverage2 = 0;
		double average1 = 0;
		double average2 = 0;
		for (int i = 0; i < firstArray.length; i++) {
		sumAverage1 += firstArray[i];
	}  for (int j = 0; j < secondArray.length; j++) {
		sumAverage2 += secondArray[j];
	} average1 = sumAverage1 / firstArray.length;
	  average2 = sumAverage2 / secondArray.length;
	  if (average1 > average2) {
		  return true;
	  } else {
		  return false;
	  }
	}

	//12. Write a method called willBuyDrink that takes a boolean isHotOutside, and a double moneyInPocket, and returns true if it is hot outside and if moneyInPocket is greater than 10.50.
	public static boolean willBuyDrink(boolean isHotOutside, double moneyInPocket) {
		if (isHotOutside == true && moneyInPocket > 10.50) {
			return true;
		} else { 
			return false;
		}
	}
	//13. Create a method of your own that solves a problem. In comments, write what the method does and why you created it.
	public static boolean canHavePuppy(boolean haveAYard, int savingsAccount) {
	if (haveAYard == true && savingsAccount > 3000) {
		return true;
	} else {
		return false;
	}
		
	}
}
//end of class
