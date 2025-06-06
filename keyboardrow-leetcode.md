# Keyboard Row - LeetCode
  
  ## Problem Description
  
  Can you solve this real interview question? Keyboard Row - Given an array of strings words, return the words that can be typed using letters of the alphabet on only one row of American keyboard like the image below.

Note that the strings are case-insensitive, both lowercased and uppercased of the same letter are treated as if they are at the same row.

In the American keyboard:

 * the first row consists of the characters "qwertyuiop",
 * the second row consists of the characters "asdfghjkl", and
 * the third row consists of the characters "zxcvbnm".

[https://assets.leetcode.com/uploads/2018/10/12/keyboard.png]
  
  ### Examples:
  ```
  Example 1:

Input: words = ["Hello","Alaska","Dad","Peace"]

Output: ["Alaska","Dad"]

Explanation:

Both "a" and "A" are in the 2nd row of the American keyboard due to case insensitivity.

Example 2:

Input: words = ["omk"]

Output: []

Example 3:

Input: words = ["adsdf","sfd"]

Output: ["adsdf","sfd"]
  ```
  
  ### Constraints:
  
  Constraints:

 * 1 <= words.length <= 20
 * 1 <= words[i].length <= 100
 * words[i] consists of English letters (both lowercase and uppercase).
  
  ### Solution Language:
  ```
  Choose a type
  ```
  
  ### Approach:
  ---

  #### approach 1:
  ```
  class Solution {

public:

    vector<string> findWords(vector<string>& words) {

        map<char, int> mp;

        vector<string> result;

        string row1 = "qwertyuiop", row2 = "asdfghjkl", row3 = "zxcvbnm";



        for (char c : row1)

            mp[c] = 1;

        for (char c : row2)

            mp[c] = 2;

        for (char c : row3)

            mp[c] = 3;



        for (auto word : words) {

            int row = mp[tolower(word[0])];

            bool valid = true;



            for (char c : word) {

                if (mp[tolower(c)] != row) {

                    valid = false;

                    break;

                }

            }



            if (valid)

                result.push_back(word);

        }



        return result;

    }

};
  ```
  