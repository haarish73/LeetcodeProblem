1984. Minimum Difference Between Highest and Lowest of K Scores



class Solution {
    public int minimumDifference(int[] nums, int k) {
      if(k==1)
      return 0;
      int n = nums.length;
      Arrays.sort(nums);
      int start  =0 ;
      int end = k-1;
      int min = Integer.MAX_VALUE;
      while(end < n){
        min = Math.min(min, nums[end] - nums[start]);
        start++;
        end++;
      }  
      return min;
    }
}
