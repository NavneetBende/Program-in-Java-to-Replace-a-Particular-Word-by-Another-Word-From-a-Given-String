Replace a Particular Word by Another Word
Today we will learn about how to replace a particular word with another Given a string and a word, the task is to remove the word from the string if it exists, otherwise, return -1, in java programming language.

Example :

input:- This is the prepinsta
Output: This is prepinsta
program in Java to replace a particular word by another word from a given string
Method 1 (Brute Force Approach)
Convert the string into a string array.
Iterate the array and check the word not equal to the given word.
Concatenate the word into a new string array name as a new string.
Print the new string.
Program to find all pairs on integer array
Run
public
class Main {
    static void remove(String str, String word) {
        String msg[] = str.split(" ");
        String new_str = "";

        // Iterating the string using for each loop
        for (String words : msg) {

            // If desired word is found
            if (!words.equals(word)) {
                // Concat the word not equal to the given word
                new_str += words + " ";
            }
        }
        // Print the new String
        System.out.print(new_str);
    }
    public
    static void main(String[] args) {
        // Custom string as input
        String str = "This is the prepinsta";
        // Word to be removed from above string
        String word = "the";
        // Calling the method 1 by passing both strings to it
        remove(str, word);
    }
}
This is prepinsta
Method 2 (String.replaceAll() Method)
This method takes two input old_word and the new word in the regex format.
Replace all the old_word with the new word.
Returns the resultant string
Code in Java
Output:
Run
public class Main
{
 public static void main(String[] args)
    {

        // Given String as input from which
        // word has to be removed
        String str = "This is the prepinsta";

        // Desired word to be removed
        String word = "the";
        // Replace all words by "" string
        // using replaceAll() method
        str = str.replaceAll("the", "");

        // Trim the string using trim() method
        str = str.trim();

        // Printing the final string
        System.out.print(str);
    }
}
Count of pairs is 3
