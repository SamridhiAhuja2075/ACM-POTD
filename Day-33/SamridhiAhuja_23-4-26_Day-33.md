## Easy Solution
```class Solution(object):
    def solve(self,cost,dp,i):
        if i<=1:
            return 0
        if dp[i]!=-1:
            return dp[i]
        dp[i]=min(self.solve(cost,dp,i-1)+cost[i-1],self.solve(cost,dp,i-2)+cost[i-2])
        return dp[i]

    def minCostClimbingStairs(self, cost):
        n=len(cost)
        dp=[-1]*(n+1)
        return self.solve(cost,dp,n)
```
![alt text](image.png)