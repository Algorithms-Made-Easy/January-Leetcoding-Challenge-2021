class Solution {
    public int numRescueBoats(int[] people, int limit) {
        //Arrays.sort(people);
        
        int[] count=new int[limit+1];
        for(int p:people){
            count[p]++;
        }
        
        int index=0;
        for(int val=1;val<=limit;val++){
            while(count[val]-->0){
                people[index++]=val;
            }
        }
        
        int left=0,right=people.length-1;
        int boats=0;
        while(left<=right){
            if(people[left]+people[right]<=limit){
                left++;
                right--;
            }
            else{
                right--;
            }
            boats++;
        }
        return boats;
    }
}
