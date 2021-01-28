class Solution {
    public String getSmallestString(int n, int k) {
        char[] c=new char[n];
        
        for(int i=n-1;i>=0;i--){
            int val= Math.min(26,k - i);
            c[i] = (char)('a'+val-1);
            k=k-val;
            
        }
        
        return new String(c);
    }
}

class Solution {
    public String getSmallestString(int n, int k) {
        
        k=k-n;
        int zcount=k/25;
        int value = k%25;
        
        char[] c=new char[n];
        int i=n-1;
        while(zcount-->0){
            c[i--]='z';
        }
        if(value>0)
            c[i--]=(char)('a'+value);
        
        while(i>=0){
            c[i--]='a';
        }
        return new String(c);
    }
}
