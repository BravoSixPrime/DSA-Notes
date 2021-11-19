## 0/1 Knapsack Prediction (No weights)
### Problem 
You have to predict whether you can for pick elements from arr to such that their sum is equal to target number

> Say : arr = [1,1,2,3,5]  target = 6

### Solution
It is possible by picking elements 1,5 or 1,2,3 so anwer is true

Using DP :

* dp[6+1]
* Initialize all elements of dp[] to false
* dp[0] = true Because 0 can be obtained by selecting nothing
* Iterate through each element of arr and for each element iterate through dp[]
* <b> if either of of dp[target] or dp[target-arr] is then true dp[target] is true </b>

```cpp
for(int i=0;i<n;i++){
  for(int j=target;j>0;j--){
      if( nums[i] <= j)
         dp[j] = dp[j] || dp[j-nums[i]];
  }
}
return dp[target];
```


        

