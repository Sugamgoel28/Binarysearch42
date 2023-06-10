<h1 align="center">Leetcode: Binary Search 42🎯</h1>

<h5 align="center"><i> Hi Stranger! I accept the Binary Search 42 challenge by LeetCode, this log will show my progress, Wish me Consistency!✨</i></h5>
<h6 align="center"><i>Let not be strangers any more? 👉<a href= "https://www.linkedin.com/in/sugam-goel-india/">Connect</a></i></h6> 
<hr>

<h3> <u>Ques 1: 704. Binary Search </u></h3>
<p>Given an array of integers nums which is sorted in ascending order, and an integer target, write a function to search target in nums. If target exists, then return its index. Otherwise, return -1.

You must write an algorithm with O(log n) runtime complexity.</p>
<pre>
<code>
class Solution {
public:
    int search(vector<int>& nums, int target) {
        
        int s = 0;
        int e = nums.size() -1;
        int mid = s + (e-s)/2;

        while(s<=e){
            if(nums[mid] == target){
                return mid;
            }
            else if(nums[mid] > target){
                e = mid - 1;
            }
            else if(nums[mid] < target){
                s = mid+1;
            }
            mid = s+(e-s)/2;
        }

        return -1;
    }
};
</code>
</pre>
