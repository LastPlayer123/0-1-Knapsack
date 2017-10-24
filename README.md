# 0-1-Knapsack


0/1 knapsack problem
 
 INTRODUCTION
     A knapsack is a bag with straps, usually carried by soldiers to help them take their valuables or things which they might need during their journey. The 0/1 knapsack problem is a very famous interview problem. The problem statement is as follows:

     Given a set of items, each of which is associated with some weight and value. Find the subset of items which can be carried into the knapsack with weight limit W. It is required that the cumulative value of the items in the knapsack is maximum value possible.

   In simple words, it asks you to pick certain items from the set of items such that their total weight is less than or equal to W and the sum of their values is maximum.

PSEUDO-CODE
The following is pseudo code for the dynamic program:

 1 // Input:
 2 // Values (stored in array v)
 3 // Weights (stored in array w)
 4 // Number of distinct items (n)
 5 // Knapsack capacity (W)
 6 
 7 for j from 0 to W do:
 8     m[0, j] := 0
 9 
10 for i from 1 to n do:
11     for j from 0 to W do:
12         if w[i] > j then:
13             m[i, j] := m[i-1, j]
14         else:
15             m[i, j] := max(m[i-1, j], m[i-1, j-w[i]] + v[i])



This solution will therefore run in  O(nW) time and O(nW) space.
