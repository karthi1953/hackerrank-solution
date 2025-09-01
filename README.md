min max sum
import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.function.*;
import java.util.regex.*;
import java.util.stream.*;
import static java.util.stream.Collectors.joining;
import static java.util.stream.Collectors.toList;

class Result {

    /*
     * Complete the 'miniMaxSum' function below.
     *
     * The function accepts INTEGER_ARRAY arr as parameter.
     */

    public static void miniMaxSum(List<Integer> arr) {
               long total = 0;
        long small = Long.MAX_VALUE;
        long large = Long.MIN_VALUE;

        for (int num : arr) {
            total += num;
        }

        for (int num : arr) {
            long currentSum = total - num; 
            if (currentSum < small) small = currentSum;
            if (currentSum > large) large = currentSum;
        }
 
        
            System.out.println(small+" "+large);


    }

}

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));

        List<Integer> arr = Stream.of(bufferedReader.readLine().replaceAll("\\s+$", "").split(" "))
            .map(Integer::parseInt)
            .collect(toList());

        Result.miniMaxSum(arr);

        bufferedReader.close();
    }
}


#Stair case

import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.function.*;
import java.util.regex.*;
import java.util.stream.*;
import static java.util.stream.Collectors.joining;
import static java.util.stream.Collectors.toList;

class Result {

    /*
     * Complete the 'staircase' function below.
     *
     * The function accepts INTEGER n as parameter.
     */

    public static void staircase(int n) {
        for(int i=1;i<=n;i++){
            System.out.println(" ".repeat(n-i)+"#".repeat(i));
        }

    }

}

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));

        int n = Integer.parseInt(bufferedReader.readLine().trim());

        Result.staircase(n);

        bufferedReader.close();
    }
}


#plus minus
import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.function.*;
import java.util.regex.*;
import java.util.stream.*;
import static java.util.stream.Collectors.joining;
import static java.util.stream.Collectors.toList;

class Result {

    /*
     * Complete the 'plusMinus' function below.
     *
     * The function accepts INTEGER_ARRAY arr as parameter.
     */

    public static void plusMinus(List<Integer> arr,int n) {
        int pos=0;
        int neg=0;
        int zer=0;
        double posf=0;
        double negf=0;
        double zerf=0;
        for(int a:arr){
            if(a<0){
                neg=neg+1;
            }
            else if(a>0){
                pos=pos+1;
            }
            else{
                zer=zer+1;
            }

        
            
        }
        posf =(double) pos/n;
        negf= (double)neg/n;
        zerf=(double)zer/n;
        System.out.printf("%.6f%n", posf);
        System.out.printf("%.6f%n", negf);
        System.out.printf("%.6f%n", zerf);


    }

}

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));

        int n = Integer.parseInt(bufferedReader.readLine().trim());

        List<Integer> arr = Stream.of(bufferedReader.readLine().replaceAll("\\s+$", "").split(" "))
            .map(Integer::parseInt)
            .collect(toList());

        Result.plusMinus(arr,n);

        bufferedReader.close();
    }
}

#Java primality test

import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.function.*;
import java.util.regex.*;
import java.util.stream.*;
import static java.util.stream.Collectors.joining;
import static java.util.stream.Collectors.toList;



public class Solution {
    public static void main(String[] args) throws IOException {
        Scanner sc = new Scanner(System.in);
        String inp=sc.nextLine();
        BigInteger num = new BigInteger(inp); 
        if(num.isProbablePrime(1)){
            System.out.println("prime");
        }else{
                        System.out.println("not prime");

        }

    }
}


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
