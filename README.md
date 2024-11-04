# Minimize-Team-Candy-Sum

You have a group of N children, and each child has a unique number of candies. Your goal is to pair them up into N/2 teams, with each team consisting of exactly 2 children. You need to find the smallest possible number, X, such that for any way you pair the children, the sum of candies in each team is no more than X.

Input
The first line of the input contains a single integer N, denoting the size of an array.
The second line of the input contains N space-separated integers, denoting the element of an array A.

Constraints
1 ≤ N ≤ 100000
1 ≤ A[i] ≤ 1000000000
Output
Print a single integer, minimum possible X.

N = int(input())
A = list(map(int, input().split()))

A.sort()

max_pair_sum = 0

for i in range(N // 2):
    pair_sum = A[i] + A[N - 1 - i]
    max_pair_sum = max(max_pair_sum, pair_sum)

print(max_pair_sum)
