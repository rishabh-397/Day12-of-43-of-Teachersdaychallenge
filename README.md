# Day12-of-43-of-Teachersdaychallenge
A. Stones on the Table
Problem Description: Given a row of n stones, each either red ('R'), green ('G'), or blue ('B'), find the minimum number of stones to remove so that no two adjacent stones have the same color.

Key Idea/Logic:

The problem can be solved with a simple greedy approach. You only need to remove stones that are the same color as their immediate predecessor.

Iterate through the stones from the second stone to the end.

Keep a counter for removed stones.

If the current stone's color is the same as the previous stone's color, you must remove the current stone to satisfy the condition. So, increment the counter.

Since you only need to remove one of the duplicates, this greedy strategy of removing the current one is optimal.

Time Complexity: O(N) where N is the number of stones, as we only need a single pass through the string.

Space Complexity: O(1) (or O(N) if the string is stored).

Example:
Input:

5
RRRRR
Output: 4
Explanation: The first 'R' can stay. The next four 'R's must be removed.

A. Boy or Girl
Problem Description: A user is male if their username has an odd number of distinct characters, and female if the number is even. Given a username string, determine the gender.

Key Idea/Logic:

The problem is about counting unique characters.

Approach:

Create a frequency array (or a set/hash map) of size 26 for the lowercase English alphabet.

Iterate through the input string. For each character, increment its count in the frequency array.

After iterating, count how many elements in the frequency array have a value greater than 0. This is the count of distinct characters.

If this count is odd, print "IGNORE HIM!". If it's even, print "CHAT WITH HER!".

Time Complexity: O(L) where L is the length of the username, as we iterate through the string and the fixed-size alphabet array.

Space Complexity: O(1) because the frequency array has a fixed size of 26.

Example:
Input: wjmzbmr
Output: CHAT WITH HER!
Explanation: The distinct characters are 'w', 'j', 'm', 'z', 'b', 'r'. The count is 6 (even), so the output is "CHAT WITH HER!".





