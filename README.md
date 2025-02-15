# [2698. Find the Punishment Number of an Integer](https://leetcode.com/problems/find-the-punishment-number-of-an-integer) (Time to Face the Consequences! 😈)

**🔴 Difficulty:** Medium 🧠 <br>
**📚 Topics Covered:** Math ➗, Backtracking 🔄
<hr>

### 🧩 A Fun Math Puzzle: Student and Teacher Discuss the Punishment Number 🔢
- ### **Student:** 
    Hey, Teacher! I have this problem: "Given a positive integer **n**, return the **punishment number** of **n**." I have no idea what a punishment number is! Can you explain? 😅

- ### **Teacher:** 
    Ah, the infamous "punishment number"! It’s not as scary as it sounds, don’t worry. Let me break it down for you.  

    A **punishment number** is defined as the sum of the squares of all integers **i** such that:  
    1. $1 \leq i \leq n$  
    2. The decimal representation of **i * i** can be split into **contiguous substrings**, and the sum of those substrings must equal **i**.  

    Sounds like a puzzle, right? But fear not, I’ll guide you through it. 🧩

- ### **Student:** 
    Whoa! Contiguous substrings? That sounds like something from a wizard’s spellbook. 🤔 Like, **i * i** is 25, so we split it into "2" and "5"? And if 2 + 5 = 7... that’s a punishment number?

- ### **Teacher:** 
    Exactly! You’re starting to catch on. Let’s say **i** = 7. Then **i * i = 49**, and you can split it into "4" and "9". If **4 + 9 = 7**, then 7 is a punishment number! 🎉  

    But here’s the twist—**you do this for all numbers** from 1 to **n**, and if they satisfy the condition, you square them and add them up. That’s the final result.   

- ### **Student:** 
    Okay, wait. I just realized this is like math *meets* a jigsaw puzzle with numbers! So, if I wanted to find the punishment number for **n = 10**, I would check every number from 1 to 10? 🔍

- ### **Teacher:** 
    Exactly! You’d start by checking 1, then 2, then 3, and so on, squaring them, looking for those magical splits. But beware, not all numbers will be punishment numbers. If they aren’t, you just ignore them. For instance, 3 squared is 9, but you can’t split 9 into anything that would sum to 3... so 3 doesn’t count. 😬

- ### **Student:** 
    So it’s like hunting for treasure in a sea of numbers, and only some of them are worth keeping! 😂

- ### **Teacher:** 
    Exactly! Some numbers are like that shiny golden coin 🪙 at the bottom of the ocean. Others? Not so much. It’s all about finding those special numbers. 🌟  

    Now, are you ready to try calculating the punishment number for a specific **n**? Or should we give a few examples to practice? 🤓

- ### **Student:** 
    I think I’m ready to dive in! Let’s go with **n = 5**. Bring on the math magic! ✨`

### 📝 Problem Statement:

Imagine you’re a number detective 🔍, and your mission is to find the **punishment number** of a given positive integer n. But wait—what is a **punishment number**, you ask? It’s a number that makes other numbers feel guilty! 😜

Here’s how it works:
- For each number **$i$** from **$1$** to **$n$**, you square it (i.e., **$i^2$**).
- Now, take the digits of **$i^2$** and split them into **contiguous chunks** (a fancy way of saying “groups of digits”).
- Add up those chunks. If the sum is equal to **$i$**, then **$i$** is a punishment number!

Your task:
- Find all the numbers **$i$** (from **$1$** to **$n$**) that meet this special condition.
- Once you find them, **square them** and **add them up**. That sum will be your final answer! 🎉

### 📚 Examples

- **Example 1:** <br>
**Input:** n = 10 <br>
**Output:** 182 <br>
**Explanation:** <br>
Alright, let’s go on a little number hunt 🕵️‍♂️. We’re looking for numbers **i** between **1** and **10** that meet our special condition. Ready? Let’s break it down:
    1. **i = 1**:  
        - Square it: 1 * 1 = 1.  
        - Can we split 1 into chunks that add up to 1? Yup! Just 1 by itself. So, 1 is a **punishment number**! ✅  
    2. **i = 9**:  
        - Square it: 9 * 9 = 81.  
        - Now, can we split 81 into chunks that add up to 9? Yes! Split it into 8 and 1. 8 + 1 = 9. So, 9 is a **punishment number** too! 🥳
    3. **i = 10**:  
        - Square it: 10 * 10 = 100.  
        - Can we split 100 into chunks that add up to 10? Yup! Split it into 10 and 0. 10 + 0 = 10. Another **punishment number**! 🎉

    So, when you add up the squares of these punishment numbers:  
    1 + 81 + 100 = **182**. 🧮

    And there you have it, the **punishment number** for **n = 10** is **182**. We’ve caught the guilty ones! 😄💥

- **Example 2:** <br>
**Input:** n = 37 <br>
**Output:** 1478 <br>
**Explanation:** <br>
Time for another number adventure! 🕵️‍♀️ This time we’re on the lookout for numbers **i** between **1** and **37** that fit the special rule. Let’s see who’s guilty! 😜
    1. **i = 1**:  
        - Square it: 1 * 1 = 1.  
        - Can we split 1 into chunks that add up to 1? Yep! 1 by itself is fine. So, 1 is a **punishment number**! ✅

    2. **i = 9**:  
        - Square it: 9 * 9 = 81.  
        - Can we split 81 into chunks that add up to 9? Of course! Split it into 8 + 1. 8 + 1 = 9. So, 9 is a **punishment number** too! 🥳

    3. **i = 10**:  
        - Square it: 10 * 10 = 100.  
        - Can we split 100 into chunks that add up to 10? Yup! Split it into 10 + 0. 10 + 0 = 10. Another **punishment number**! 🎉

    4. **i = 36**:  
        - Square it: 36 * 36 = 1296.  
        - Can we split 1296 into chunks that add up to 36? You bet! Split it into 1 + 29 + 6. 1 + 29 + 6 = 36. So, 36 is a **punishment number** as well! 🌟

    Now, we add up the squares of these punishment numbers:  
    1 + 81 + 100 + 1296 = **1478**. 🎯

    And there you go, the **punishment number** for **n = 37** is **1478**! We’ve found the guilty numbers! 😄💥

### 📏 Constraints
- **$1 \le n \le 100$** 🚀  
    - This means that the value of **n** (the number we are looking at) will always be a positive integer between **1** and **100**. So, no super huge numbers to worry about—just a nice range where we can do some fun calculations! 😄
    - Think of it like this: You won’t have to handle any crazy, gigantic numbers, but you’ll still get to test your number detective skills with numbers as big as 100! 💡

    Don't worry, it's manageable! You're ready for this challenge. 💪📈

### 💡 Hints
- **Can we generate all possible partitions of a number?** 🤔  
    - Yes! You can split a number into different parts. It’s like trying to break a big number into smaller chunks. For example, 81 can be split into 8 and 1 or just 81 by itself. You just need to figure out how to make all possible ways of splitting the number. 🤯

- **Use a recursive algorithm that splits the number into two parts, generates all possible partitions of each part recursively, and then combines them in all possible ways.** 🔄  
    - Think of it like a branching tree 🌳! Start with a number, then break it into two parts. Next, recursively do the same thing with those parts and keep splitting. Finally, combine all the parts in different ways to get the different partitions. 🧩

    It’s a bit like playing with puzzles 🔍. Break the pieces down and put them back together in all sorts of combinations!