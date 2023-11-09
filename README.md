# Sort-the-People-using-java-Leetcode

    import java.util.*;
    class Solution {
        public String[] sortPeople(String[] names, int[] heights) {
            HashMap<Integer,String> map = new HashMap<>();
            int n = heights.length;
            for(int i =0; i<n;i++){
                map.put(heights[i],names[i]);
            }
            Arrays.sort(heights);
            String[] str = new String[n];
            int k,j;
            for(j =n-1,k=0; j>=0;j--,k++){
                str[k] = map.get(heights[j]);
            }
            return str;
    
        }
    }
