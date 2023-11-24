This Java program checks the validity of a credit card number using Luhn's algorithm. The program takes an n-digit credit card number as input, where the last digit is the check digit. It then determines if the credit card number is valid or not based on Luhn's algorithm.

Luhn's Algorithm
Luhn's algorithm is used to verify credit card numbers. The steps involved are:

From the rightmost digit (check digit) and moving left, double the value of every second digit.
If the result of the doubling operation is greater than 9, add the digits of the product, or alternatively, subtract 9 from the product.
Take the sum of all the digits.
If the total modulo 10 is equal to 0 (ends in zero), the number is valid according to Luhn's formula.
Input Format
An n-digit credit card number, where the last digit is the check digit.

Output Format
Output "VALID" if it is a valid credit card number and "INVALID" if it is not.

Constraints
4 <= n <= 30
Sample Input
plaintext
Copy code
4539682995824395
Sample Output
plaintext
Copy code
VALID
Explanation
Read from right to left:

Every second digit from the last digit: 5 + 3 + 2 + 5 + 9 + 8 + 9 + 5 = 46
Double every second digit from the second last digit and subtract 9 if needed:
2 * 9 = 18; 18 - 9 = 9
2 * 4 = 8
2 * 8 = 16; 16 - 9 = 7
2 * 9 = 18; 18 - 9 = 9
2 * 2 = 4
2 * 6 = 12; 12 - 9 = 3
2 * 3 = 6
2 * 4 = 8
Adding these together: 46 + 54 = 100
100 % 10 == 0, so the card is VALID.
