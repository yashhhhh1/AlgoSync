# Same Tree - LeetCode
  
  ## Problem Description
  
  Can you solve this real interview question? Same Tree - Given the roots of two binary trees p and q, write a function to check if they are the same or not.

Two binary trees are considered the same if they are structurally identical, and the nodes have the same value.
  
  ### Examples:
  ```
  Example 1:

[https://assets.leetcode.com/uploads/2020/12/20/ex1.jpg]


Input: p = [1,2,3], q = [1,2,3]
Output: true


Example 2:

[https://assets.leetcode.com/uploads/2020/12/20/ex2.jpg]


Input: p = [1,2], q = [1,null,2]
Output: false


Example 3:

[https://assets.leetcode.com/uploads/2020/12/20/ex3.jpg]


Input: p = [1,2,1], q = [1,1,2]
Output: false
  ```
  
  ### Constraints:
  
  Constraints:

 * The number of nodes in both trees is in the range [0, 100].
 * -104 <= Node.val <= 104
  
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

    bool test(TreeNode* p, TreeNode* q) {

        if (q == NULL && p == NULL)

            return true;

        if (q == NULL || p == NULL)

            return false;

        return (p->val == q->val) && test(p->left, q->left) &&

               test(p->right, q->right);

    }

    bool isSameTree(TreeNode* p, TreeNode* q) {return test(p, q); }

};
  ```
  