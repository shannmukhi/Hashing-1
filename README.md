# Hashing-1

## Problem 1:
Given an array of strings, group anagrams together.

Example:
Input: ["eat", "tea", "tan", "ate", "nat", "bat"],
Output:
[
  ["ate","eat","tea"],
  ["nat","tan"],
  ["bat"]
]

Note:
All inputs will be in lowercase.
The order of your output does not matter.
Program:
//First  convert the string to individual characters and compare all the other strings in array.If it matches return true
class Solution {
    public List<List<String>> groupAnagrams(String[] strs) {
        Map<String, List> ans = new HashMap<String, List>();
        for (String s : strs) {
            char[] ca = s.toCharArray();
            Arrays.sort(ca);
  }
           
## Problem 2:
Given two strings s and t, determine if they are isomorphic.
Two strings are isomorphic if the characters in s can be replaced to get t.
All occurrences of a character must be replaced with another character while preserving the order of characters. No two characters may map to the same character but a character may map to itself.

Example 1:
Input: s = "egg", t = "add"
Output: true

Example 2:
Input: s = "foo", t = "bar"
Output: false

Example 3:
Input: s = "paper", t = "title"
Output: true
Note:
You may assume both s and t have the same length.
// break the word into individual strings and compare now map them if it occurs again check if it is the same one mapped the first time. 
    static boolean areIsomorphic(String str1, String str2) 
    { 
       Boolean[] marked = new Boolean[size]; 
        Arrays.fill(marked, Boolean.FALSE); 
        int[] map = new int[size]; 
        Arrays.fill(map, -1);  
        for (int i = 0; i < n; i++) 
        { 
           
  if (map[str1.charAt(i)] == -1) 
            { 
                 
  if (marked[str2.charAt(i)] == true) 
                    return false; 
  marked[str2.charAt(i)] = true; 
  map[str1.charAt(i)] = str2.charAt(i); 
            }
 else if (map[str1.charAt(i)] != str2.charAt(i)) 
            return false;  
            }return true; 
    } 


## Problem 3:
Given a pattern and a string str, find if str follows the same pattern.
Here follow means a full match, such that there is a bijection between a letter in pattern and a non-empty word in str.

Example 1:
Input: pattern = "abba", str = "dog cat cat dog"
Output: true

Example 2:
Input:pattern = "abba", str = "dog cat cat fish"
Output: false

Example 3:
Input: pattern = "aaaa", str = "dog cat cat dog"
Output: false

Example 4:
Input: pattern = "abba", str = "dog dog dog dog"
Output: false
Notes:
You may assume pattern contains only lowercase letters, and str contains lowercase letters that may be separated by a single space.
Program:
//consider string and break into list of individual char and then split the array into list of words and start mapping if it is the second time seen it should match to the first time mapped one else return false 
