# Leetcode-6.-Zigzag-Conversion
# Description
The string "PAYPALISHIRING" is written in a zigzag pattern on a given number of rows like this: (you may want to display this pattern in a fixed font for better legibility)

P   A   H   N

A P L S I I G

Y   I   R
And then read line by line: "PAHNAPLSIIGYIR"

Write the code that will take a string and make this conversion given a number of rows:

string convert(string s, int numRows);
# Solution
In the given problem, we have to rearrange the characters of a string in a zigzag pattern over a given number of rows, and then read the characters row by row to form the final string.

This can be done by :

a. If numRows == 1, no zigzag can form, so return the string as is.

b. Zigzag characters follow a repeating cycle of length increment = (numRows - 1) * 2.

c. Row 0 and Row numRows-1: characters are spaced exactly increment apart.

d. Middle rows: each cycle contributes two characters to the row — one from the vertical down stroke (s[i]) and one from the diagonal upward stroke (s[i + increment - 2*r]), which must be checked to stay within bounds.

e. Iterate row by row, appending characters based on this pattern until the end of the string.

![IMG_9921](https://github.com/user-attachments/assets/610fd025-b50f-4540-8212-20e9e14b105d)

![IMG_9922](https://github.com/user-attachments/assets/1e97cbe7-7ecf-4cc7-bdf4-ce35965d42ce)
