# Binary Tree Inorder Traversal - LeetCode
  
  ## Problem Description
  
  Can you solve this real interview question? Binary Tree Inorder Traversal - Given the root of a binary tree, return the inorder traversal of its nodes' values.
  
  ### Examples:
  ```
  Example 1:

Input: root = [1,null,2,3]

Output: [1,3,2]

Explanation:

[https://assets.leetcode.com/uploads/2024/08/29/screenshot-2024-08-29-202743.png]

Example 2:

Input: root = [1,2,3,4,5,null,8,null,null,6,7,9]

Output: [4,2,6,5,7,1,3,9,8]

Explanation:

[https://assets.leetcode.com/uploads/2024/08/29/tree_2.png]

Example 3:

Input: root = []

Output: []

Example 4:

Input: root = [1]

Output: [1]
  ```
  
  ### Constraints:
  
  Constraints:

 * The number of nodes in the tree is in the range [0, 100].
 * -100 <= Node.val <= 100

 

Follow up: Recursive solution is trivial, could you do it iteratively?
  
  ### Solution Language:
  ```
  Choose a type
  ```
  
  ### Approach:
  ---

  #### approach 1:
  ```
  /**

 * Definition for a binary tree node.

 * struct TreeNode {

 *     int val;

 *     TreeNode *left;

 *     TreeNode *right;

 *     TreeNode() : val(0), left(nullptr), right(nullptr) {}

 *     TreeNode(int x) : val(x), left(nullptr), right(nullptr) {}

 *     TreeNode(int x, TreeNode *left, TreeNode *right) : val(x), left(left),

 * right(right) {}

 * };

 */

class Solution {

public:

    void inorderTraversal(TreeNode* root, vector<int>& result) {

        if (root == nullptr)

            return;



        inorderTraversal(root->left, result);

        result.push_back(root->val);

        inorderTraversal(root->right, result);

    }

    vector<int> inorderTraversal(TreeNode* root) {



        vector<int> result;

        inorderTraversal(root, result);

        return result;

    }

};
  ```
  