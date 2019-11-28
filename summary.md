## 1. Two Sum ##
Dict, key is target-nums[index], value is index.

## 4. Median of Two Sorted Arrays ##
binary search, 
generally, an array of length N can regarded as:
		
	new = #a1#a2#...a3#"        //has length 2*N+1
if we want to cut the array, we have index(L) = (CutPosition-1)/2, index(R) = (CutPosition)/2.
L, R are number on the both sides of the cut.(if Cut Position is a number, index(L) = index(R))

## 5. Longest Palindromic Substring ##
Manacher's Algorithm

## 10. Regular Expression Matching ##
DP, recursive up to bottom

## 41. First Missing Positive ##
place numbers as many as possible to the right place, each step can not make the result worse.
	
	while(i<n){
        if(nums[i] > 0 && nums[i] < n && nums[i] != nums[nums[i]-1]){
            t = nums[i];
            nums[i] = nums[t-1];      
            nums[t-1] = t;         
        }
        else
            i++;
    }

## 310. Minimum Height Trees ##
Remove leaf nodes layer by layer, so that there will be only one or two nodes left. we can use "set" as adjacency list.

