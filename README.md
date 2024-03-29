# Plagiarism-Detector
Team members:

Divyajot Kaur Dadiala

Robert Barnstead

Jusnoor Kaur Sachdeva

## Milestone 1
For this milestone our team will be describing the first algorithm that we will use for
our plagiarism detector. We shall be working on the Knuth-Morris-Pratt (KMP) string
searching algorithm. We shall be describing the algorithm problem, writing a pseudo
code, providing an analysis and listing the unexpected cases and difficulties.

## Milestone 2
For this milestone our team will be describing the second that we will use for our
plagiarism detector. We shall be working on the LCSS algorithm. We shall be
describing the algorithm problem, writing a pseudo code, providing an analysis and
listing the unexpected cases and difficulties.

## Milestone 3
The KMP Algorithim has been designed to take two strings a text string and a pattern string and determine whether the pattern appears in the text. To implement this we took the dataset provided and read the CSV file using openCSV in Java to create one giant string of text. To define our pattern we randomly took one of the entries from the text that was found while reading the CSV file and stored it as a string. Then we called the search function using both the text and pattern. In the search function we call the LPS function in order to create the LPS array that assists us in finding the pattern in the string. This returns us the Char range where the pattern is found, or in our case where plagiarism has been found. A major issue that we ran into was the time it takes to create the string.

The LCS Algorithm takes two strings A which is the text and B which is the pattern and checks for the longest common sub sequence. This is done using a 2d array of size [len(B)+1][len(A)+1] called check that gets filled retroactively. This is done by initializing each value to 0 then checking whether the value at A[i-1] and B[j-1] match, if they do we set check[i][j] equal to the value at check[i-1][j-1]+1. This increases the longest common subsequence by 1. If they are not a match we set the longest common subsequence eqaul to the max between A[i-1][j] or B[i][j-1]. Finally we return the value at check[a][b] or the last value in the array which is our longest commmon subsequence value.

## Milestone 4
In this project, we are building a plagiarism detector and comparing three
different algorithms KMP, LCS, and RabinCarp fingerprints. All three algorithms
can be used to detect plagiarism in a text.
