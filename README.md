# LeetCode1
题目描述

给定一个整数数组 nums 和一个目标值
target，请你在该数组中找出和为目标值的那 两个 整数，并返回他们的数组下标。你可以假设每种输入只会对应一个答案。但是，你不能重复利用这个数组中同样的元素。

![image](F:/%E6%9C%89%E9%81%93%E7%AC%94%E8%AE%B0/%E6%9C%89%E9%81%93%E5%9B%BE%E7%89%87%E7%AC%94%E8%AE%B0/1.png)
解题思路：
这个题目第一眼一看首先想到的是暴力解决，采用2重循环，类似于双指针的解法，结果是可以通过的，具体代码如下：
```
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
```
对于上面暴力解法，一般在算法题里面是会超时的

