#Valid username regular expression

import java.io.*;
import java.util.*;

public class Solution {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = Integer.parseInt(sc.nextLine()); 
     
        for(int i=0;i<n;i++){
        String inp = sc.nextLine();
        
        if(inp.matches("^[a-zA-Z]\\w{7,29}$")){
            System.out.println("Valid");
        }
        else{
            System.out.println("Invalid");

           }
              }
    }
}
#Java regex
import java.io.*;
import java.util.*;

class MyRegex{
    
    public String pattern =
        "^(25[0-5]|2[0-4][0-9]|1[0-9]{2}|0[0-9]{2}|[0-9]{1,2})"
      + "(\\.(25[0-5]|2[0-4][0-9]|1[0-9]{2}|0[0-9]{2}|[0-9]{1,2})){3}$";
}

    

public class Solution {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        MyRegex obj = new MyRegex();
        
        while(sc.hasNext()){
           String ip= sc.next();
           System.out.println(ip.matches(obj.pattern));
        

    }
    sc.close();
    }
}

#Pattern syntax checker

import java.io.*;
import java.util.*;
import java.util.regex.*;
public class Solution {

    public static void main(String[] args) {
        
        Scanner sc = new Scanner(System.in);
        int totalinp = sc.nextInt();
        sc.nextLine();
        for(int i =0;i<totalinp;i++){
            String inp = sc.nextLine();
            try{
               Pattern.compile(inp);
               System.out.println("Valid");
            }catch(PatternSyntaxException e){
                  System.out.println("Invalid");

            }
        }
        sc.close();

    }
}

#Java String Tokens

import java.io.*;
import java.util.*;

class Splits {
    int count1 = 0;
    List<String> tokens = new ArrayList<>();

    public void splits1(String inp) {
        String[] arr = inp.split("[^A-Za-z]+");
        for (String a : arr) {
            if (!a.isEmpty()) {
                tokens.add(a);
                count1++;
            }
        }
    }

    void counts() {
        System.out.println(count1);
    }

    public void prints() {
        for (String a : tokens) {
            System.out.println(a);
        }
    }
}

public class Solution {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String inp = sc.nextLine();

        Splits obj1 = new Splits();
        obj1.splits1(inp);
        obj1.counts();
        obj1.prints();
    }
}
