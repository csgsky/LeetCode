# 1. Two Sum

题目描述：
        Given an array of integers, return indices of the two numbers such that they add up to a specific target.You may assume that each input would have exactly one solution.
        中文：给定一个整形数组，根据某个给定的具体值，找出数组两个数字相加恰好等于给定的值的指数，假设你每次输入都只有一个解。
例子：
---
        Given nums = [2, 7, 11, 15], target = 9,
        Because nums[0] + nums[1] = 2 + 7 = 9,
        return [0, 1].

答案：
---

    public class Solution {
         public int[] twoSum(int[] nums, int target) {
             int [] res = new int[2];
             if(nums==null || nums.length<2)
             return res;
             HashMap<Integer,Integer> map = new HashMap<Integer,Integer>();
             for(int i = 0; i < nums.length; i++){
                if(!map.containsKey(target-nums[i])){
                        map.put(nums[i],i);
                    }else{
                        res[0]= map.get(target-nums[i]);
                        res[1]= i;
                        break;
                 }
             }
                return res;
         }
    }





