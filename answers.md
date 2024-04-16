# CMPS 2200 Assignment 3
## Answers

**Name:**_____Josh Allison ____________________

1a) Given a $N$ dollars, state a greedy algorithm for producing as few coins as possible that sum to $N$.
We are assuming 2**k is the highest currency we have and k does not go less than 0, we can use an algorithm like this. 
We start with the largest power of 2 that lies in N, subtract as many as possible of that number from N and then move onto the next largest denomination, and so on, until the coins subtracted total to the number N. 


1b) Prove that this algorithm is optimal by proving the greedy choice and optimal substructure properties.

The algorithm is optimal because it selects as many of the largest 2^k coins as possible before moving onto the next denomination which makes it greedy. It reduces the amount of times a coin has to be picked, and each time a new coin needs to be picked gives the function a new problem of subtracting the next largest 2^k which makes it optimal.



1c) What is the work and span of your algorithm?
The work is O(logn) and the span is also O(logn).



2a) You realize the greedy algorithm you devised above doesn't work in Fortuito. Give a simple counterexample that shows that the greedy algorithm does not produce the fewest number of coins.

A counter example that works for this is if the denominations are: D0 = 1 D1 = 3 D2 = 4
and
N = 6

The Greedy function takes largest D2, remaining N is 2. Fulfilled by taking 2 denominations of D0. Total 3 coins:
from common sense, we know that 2 coins is the minimum number so this is an example where the greedy algorithm did not produce the fewest number of coins. 

2b) Since you paid attention in Algorithms class, you realize that while this problem does not have the greedy choice property it does have an optimal substructure property. State and prove this property. 
The optimal subsctircture property of this problem will be the minimum ammount of coins needed to get from 0 to n dollars. 


2c) Use this optimal substructure property to design a dynamic programming algorithm for this problem. If you used top-down or bottom-up memoization to avoid recomputing solutions to subproblems, what is the work and span of your approach?

The work is O(N*k), as each subproblem multiplies the number of denominations by the goal number. The span will be the longest run in the chart will will be O(n)

Part 3: Edit Distance


3a) The code for MED from the lecture notes is provided as a starting point in main.py. Now implement fast_MED, a top-down memoized version of MED. Test your implementation code using test_MED.


3b) Now that you have implemented an efficient algorithm for computing edit distance, let's turn to the problem of identifying the actual edits between two sequences.


Implement fast_align_MED to return the aligned versions of $S$ and $T$, and test your code with test_alignment.
