{
    "question":"1. Two Sum Solved Easy TopicsCompaniesHintGiven an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.You may assume that each input would have exactly one solution, and you may not use the same element twice.You can return the answer in any order. Example 1:Input: nums = [2,7,11,15], target = 9Output: [0,1]Explanation: Because nums[0] + nums[1] == 9, we return [0, 1].Example 2:Input: nums = [3,2,4], target = 6Output: [1,2]Example 3:Input: nums = [3,3], target = 6Output: [0,1] Constraints:2 <= nums.length <= 104-109 <= nums[i] <= 109-109 <= target <= 109Only one valid answer exists.",
    "answer":"class Solution {public:vector<int> twoSum(vector<int>& nums, int target) {map<int, int> mp;vector<int> final_sum;for (int i = 0; i < nums.size(); i++) {int remaing_sum = target - nums[i];if (mp.find(remaing_sum) != mp.end()) {final_sum.push_back(i);final_sum.push_back(mp[remaing_sum]);return final_sum;}mp[nums[i]] = i;}return final_sum;}};", 
    "language":"c++",
    "Problem_Name":"Two Sum", "
    token":"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" 
}
