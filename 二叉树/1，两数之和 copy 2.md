# 1，两数之和
#### April 7,10:00 2023


> A tech blog,taizilaoren leetcode⚡⚡⚡.
> Let's start it ⚡⚡⚡.
> 一日一题，进步每天 📔📕📖📗📘📙📚📓📒📃📜📄🔖🍊🍋🍎🍑🍉🥦🌽🥙🤩😚🤗.

## 题目简述
给定一个整数数组 nums 和一个整数目标值 target，请你在该数组中找出 和为目标值 target  的那 两个 整数，并返回它们的数组下标。
## 题目思路
- 1，双循环
- 2，哈希表
    - 注意key是数组的值，因为map的方法get，has都是对应的key

## 题目解答

```js
function twoSum(nums, target) {
    const hashMap = new Map();
    
    for (let i = 0; i < nums.length; i++) {
        const complement = target - nums[i];
        
        if (hashMap.has(complement)) {
            return [hashMap.get(complement), i];
        }
        
        hashMap.set(nums[i], i);
    }
    
    return [];
}
```