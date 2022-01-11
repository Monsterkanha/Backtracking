# Backtracking
Here, I will post backtracking famous problem. 


Backtracking has general structure. 

public List<List<Integer>> subsets(int[] nums) {
    List<List<Integer>> list = new ArrayList<>();
    Arrays.sort(nums);
    backtrack(list, new ArrayList<>(), nums, 0);
    return list;
}

private void backtrack(List<List<Integer>> list , List<Integer> tempList, int [] nums, int start){
    list.add(new ArrayList<>(tempList));
    for(int i = start; i < nums.length; i++){
        tempList.add(nums[i]);
        backtrack(list, tempList, nums, i + 1);
        tempList.remove(tempList.size() - 1);
    }
}
                                        
                                        
First add current element and then call recursively and after returning remove that. 
Why to remove since we will pass by reference. 
 
                                        
                                  

                                        
                                        
 
