# leetcode-
记录大概一年来在LeetCode上做的题目，顺便总结下
···java
class Solution{ 
    public int[] twoSum(int[] nums, int target){
        for(int i=0;i<nums.length-1;i++){
            for(int j=i+1;j<nums.length;j++){
                if(nums[j]==target-nums[i]){
                    return new int[]{i,j};
                }
            }
        }
        //因为最终要有返回值
        throw new IllegaArgumentEXCEPTION("没有满足条件的结果");
    }
}
···


