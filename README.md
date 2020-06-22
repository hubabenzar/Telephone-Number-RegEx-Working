# Telephone-Number-RegEx-Working
This Regular Expression (RegEX) is my solution to a telephone number that is flexible to be used by most people.

It allows for the use of extensions or ext at any point in the code.
The only requirment is for the input/string to contain three characters with the option of having spaces in between, but not symbols or alpha numericals.

Feel free to let me know if this code can be improved.

Code:
^[\W\d]*(?:\s*\d\s*){3,}(?:\W*ext(ension)*\W*\d*)*$

Explanation attached in file.

Test it out:
regexr.com/5753o
