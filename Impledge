import java.io.*;
import java.lang.*;
import java.util.*;
class HelloWorld {
    public static void main(String[] args) throws IOException{
     Scanner sc=new Scanner(System.in);
     int n=sc.nextInt();
String[] str=new String[n];
sc.nextLine();
   for(int i=0 ; i<n ; i++){
    str[i]=sc.nextLine();
   }
   Arrays.sort(str,Comparator.comparingInt(String::length));
   HashMap<String,Integer> map=new HashMap<>();
   for(String s:str){
       if(map.containsKey(s))
       map.put(s,map.get(s)+1);
       else map.put(s,1);
   }
   int count=0;
   for(int i=n-1 ; i>=0 ; i--){
     StringBuffer sb=new StringBuffer();
    int c=0;
     for(int j=str[i].length()-1 ; j>=0 ; j--){
      sb.append(str[i].charAt(j));
      if(map.containsKey(sb.reverse().toString()))
          {  
            if((sb.toString()).equals(str[i]))
            continue;
           sb.delete(0,sb.length());
           c=0;
          }
      else{
          sb.reverse();
          c++;
           }
       }
      if(c==0){
        count++;
        if(count==1)
        System.out.println("Longest Compund Word: "+str[i]);
        else if(count==2)
        System.out.println("Second Longest Compound Word: "+str[i]);
     }
     System.out.println();
     if(count==2)
     break;
  }
 }
}
