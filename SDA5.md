# TEME BACK-END 📚

## Algoritmi pentru interviuri

### Algoritmi string-uri

#### 1. Given a List of Maps, write a method to average each of the properties independently. 
Exclude null values from the average in the parameter data. 
Example data: -
[ { "temperature": 44, "humidity": 12 }, { "temperature": 23, "humidity": 34 }, { "temperature": 34 } ,{ "temperature": null }]
The return value should be a single Map containing the averages, e.g.
{"temperature": 21.0,“humidity”: 33}

#### 2. We have a process that imports a set of product codes into a database, however recently we have noticed that several of the codes have not been formatted correctly and due to the age of the system these are not validated before the import.
Implement product code validation
Our import process already reads the file and adds them into the database, however, there is no validation. Create a validation routine that can be called from the existing code.
Product codes
Our product codes are 7 digits long and have the format:
AANNNYY
AA is 2 alpha characters and NNN is 3 numeric characters and together they form the product ID.
YY is the offer suffix.


#### 3. Given two strings s and t, determine if they are isomorphic.

Two strings s and t are isomorphic if the characters in s can be replaced to get t.

All occurrences of a character must be replaced with another character while preserving the order of characters. No two characters may map to the same character, but a character may map to itself.

Example 1:

Input: s = "egg", t = "add"
Output: true
Example 2:

Input: s = "foo", t = "bar"
Output: false
Example 3:

Input: s = "paper", t = "title"
Output: true



#### 4. Given a list of words and two words: word1 and word2, return the shortest distance between these two words in the list.
Example:
Assume that words =["practice", "makes", "perfect", "coding", "makes"].
Input: word1 = “coding”, word2 = “practice”
Output: 3
Input: word1 = "makes", word2 = "coding"
Output: 1


#### 5. You are playing the following Flip Game with your friend: Given a string that contains only two characters: + and -, you can flip two consecutive "++" into "--", you can only flip one time. Please find all strings that can be obtained after one flip.

Write a program to find all possible states of the string after one valid move.

Example
Example1

Input:  s = "++++"
Output: 
[
  "--++",
  "+--+",
  "++--"
]
Example2

Input: s = "---+++-+++-+"
Output: 
[
	"---+++-+---+",
	"---+++---+-+",
	"---+---+++-+",
	"-----+-+++-+"
]


#### 6. How do you find the length of the longest substring without repeating characters?
#### 7. How do you find the longest palindromic substring in str?
#### 8. Longest common prefix













