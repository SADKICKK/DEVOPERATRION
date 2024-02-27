import java.util.HashMap;
import java.util.Map;
class Solution {
    public int[] twoSum(int[] nums, int target) {
        
        Map< Integer ,Integer > numMap =new HashMap<>();
        for ( int i=0; i<=nums.length ; i++)
        {
            int c = target -nums[i];
            if ( numMap.containsKey(c))
            {
                return new int[]{ numMap.get(c),i};
            }
                else
                {
                    numMap.put(nums[i],i);
                }
            
        }
        return new int[]{};
    }
}
