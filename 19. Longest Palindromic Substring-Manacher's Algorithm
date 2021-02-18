class Solution {
    public String longestPalindrome(String s) {
        int n=s.length();
        char[] newStr=new char[2*n+1];
        int i=0;
        newStr[i++]='#';
        for(char c:s.toCharArray()){
            newStr[i++]=c;
            newStr[i++]='#';
        }
        
        int p[]=new int[2*n+1];
        int center=0,right=0;
        
        int longestLength=0,longestCenter=0;
        
        for(i=0;i<newStr.length;i++){
            
            int mirror= 2*center-i;
            
            if(right>i){
                p[i]=Math.min(p[mirror],right-i);
            }
            
            int a=i + (p[i]+1);
            int b=i - (p[i]+1);
            
            while(b>=0 && a<newStr.length && newStr[a]==newStr[b]){
                b--;
                a++;
                p[i]++;
            }
            
            if(p[i]>=longestLength){
                longestCenter=i;
                longestLength=p[i];
            }
            
            if(i+p[i]>right){
                center=i;
                right=i+p[i];
            }
        }
        
        String st=new String(newStr);
        return st.substring(longestCenter-longestLength,longestCenter+longestLength).replace("#","");
    }
}
