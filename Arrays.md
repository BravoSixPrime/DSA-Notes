## Maximum Product Subarray
https://leetcode.com/problems/maximum-product-subarray/

TC: O(n) SC:O(1)
* Assign r = nums[0];
* Keep 2 variables imax,imin which are max till this cell and min till this cell resp.
* Initially both are r
* If incoming nums[i] is negative : swap imax and imin
* Update imax and imin 
  * imax = max(nums[i],imax)
  * imin = min(nums[i],imin)
* r = max(r,imax)
* Return r 
