
#Sales by match
class Result {
    
    public static int linear(List<Integer> ar,int target,int index){
        
        for (int i = index+1; i < ar.size(); i++) {
            if(ar.get(i)==target){
                return i;
            }
        }
                    return -1;
    }

   

    public static int sockMerchant(int n, List<Integer> ar) {
        int pair=0;
        for (int j = 0; j < ar.size(); j++) {
             int val=linear(ar,ar.get(j),j);
             if(ar.get(j)==-99){
                continue;
             }
            if(val>=0){
                pair++;
                ar.set(val, -99);
                ar.set(j,-99);
            }
        }
           

        
        return pair;

    }

}
#Divisible sum pairs
public static int divisibleSumPairs(int n, int k, List<Integer> ar) {
       int count=0;
        for (int i = 0; i < n; i++) {
            for (int j = i+1; j < n; j++) {
                if((ar.get(i)+ar.get(j))%k==0){
                    count++;
                }
            }
        }
            return count;
    }

}
#Cats and Mouse
public class Solution {
    static String catAndMouse(int a, int b, int m) {
    
        int dista=m-a;
        int distb=m-b;
        if(dista<0){
            dista=dista*(-1);
        }
        if(distb<0){
            distb=distb*(-1);
        }
        
        if(dista>distb){
            return "Cat B";
        }
        if(dista<distb){
            return "Cat A";
        }
        return "Mouse C";
    }
#Migratory birds

public static int migratoryBirds(List<Integer> arr) {
        int[] countarr= new int[6];

        for(int a:arr){
            countarr[a]++;
        }
        int ans=1;
        int maxv=countarr[1];
        for(int i=2;i<countarr.length;i++){
           if(countarr[i]>maxv){
            maxv=countarr[i];
              ans=i;
           }
        }
            return ans;
    }


#Day of programmer
    public static String dayOfProgrammer(int year) {
        
        if(year==1918){
            return "26.09.1918";
        }
        if(year<1918){
            if(year%4==0){
            return "12.09."+year;
        }else{
             return "13.09."+year;

        }
        }
        if(year>1918){
        if(year%400==0 || year%4==0&&year%100!=0){
            return "12.09."+year;
        }else{
             return "13.09."+year;

        }   
        }

            return "Wrong input";
    }

}

#Bill division
class Result {

    public static void bonAppetit(List<Integer> bill, int k, int b) {
        int add=0;
        for (int i = 0; i < bill.size(); i++) {
            if(i!=k){
                add=add+bill.get(i);
            }
        }
        add=add/2;
        if(add==b){
            System.out.println("Bon Appetit");
        }else{
        System.out.println(b-add);

        }


    }

}


#Java arraylist
import java.io.*;
import java.util.*;

public class Solution {

    public static void main(String[] args) {
        /* Enter your code here. Read input from STDIN. Print output to STDOUT. Your class should be named Solution. */
        
        Scanner sc=new Scanner(System.in);
        
        int n=sc.nextInt();
        int[][] arr=new int[n][];

        for (int i = 0; i <n ; i++) {
            int nn=sc.nextInt();
            arr[i]=new int[nn];
            for (int j = 0; j < nn; j++) {
                
                arr[i][j]=sc.nextInt();

            }
        }
        int n2=sc.nextInt();
        

        for (int i = 0; i <n2; i++) {
            int x=sc.nextInt();
            int y=sc.nextInt();
            try{
                System.out.println(arr[x-1][y-1]);
            }catch(Exception e){
                System.out.println("ERROR!");
            }
        }
    
        
    }
}

#Breaking the records
    public static List<Integer> breakingRecords(List<Integer> scores) {
        int hs=scores.get(0);
        int ls=scores.get(0);
        int hschanges=0;
        int lschanges=0;
        List<Integer> ret=new ArrayList<Integer>();
        for (int i = 0; i < scores.size(); i++) {
            
            if(hs<scores.get(i)){
                hs=scores.get(i);
                hschanges++;
            }else if(ls>scores.get(i)){
                ls=scores.get(i);
                lschanges++;

            }


        }
        ret.add(hschanges);
        ret.add(lschanges);
        return ret;

    }

# Number line jumbs (kangaroo)
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
     * Complete the 'kangaroo' function below.
     *
     * The function is expected to return a STRING.
     * The function accepts following parameters:
     *  1. INTEGER x1
     *  2. INTEGER v1
     *  3. INTEGER x2
     *  4. INTEGER v2
     */

    public static String kangaroo(int x1, int v1, int x2, int v2) {
    if (x1 < x2 && v1 <= v2) return "NO";
    if (x2 < x1 && v2 <= v1) return "NO";

    if ((x2 - x1) % (v1 - v2) == 0) return "YES";

    return "NO";


    }

}

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter bufferedWriter = new BufferedWriter(new FileWriter(System.getenv("OUTPUT_PATH")));

        String[] firstMultipleInput = bufferedReader.readLine().replaceAll("\\s+$", "").split(" ");

        int x1 = Integer.parseInt(firstMultipleInput[0]);

        int v1 = Integer.parseInt(firstMultipleInput[1]);

        int x2 = Integer.parseInt(firstMultipleInput[2]);

        int v2 = Integer.parseInt(firstMultipleInput[3]);

        String result = Result.kangaroo(x1, v1, x2, v2);

        bufferedWriter.write(result);
        bufferedWriter.newLine();

        bufferedReader.close();
        bufferedWriter.close();
    }
}

#Apple and orange

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
     * Complete the 'countApplesAndOranges' function below.
     *
     * The function accepts following parameters:
     *  1. INTEGER s
     *  2. INTEGER t
     *  3. INTEGER a
     *  4. INTEGER b
     *  5. INTEGER_ARRAY apples
     *  6. INTEGER_ARRAY oranges
     */

    public static void countApplesAndOranges(int s, int t, int a, int b, List<Integer> apples, List<Integer> oranges) {
        int appletotal=0;
        for (int i = 0; i < apples.size(); i++) {
            int appleadd;
            appleadd=a+apples.get(i);
            
            if(appleadd>=s&&t>=appleadd){
                appletotal++;
                
            }
        }
        int orangetotal=0;
        for (int j = 0; j < oranges.size(); j++) {
            int orangesadd;
            orangesadd=b+oranges.get(j);
            
            if(orangesadd>=s&&t>=orangesadd){
                orangetotal++;
                
            }
        }
        System.out.println(appletotal);
        System.out.println(orangetotal);
        
    

    }

}

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));

        String[] firstMultipleInput = bufferedReader.readLine().replaceAll("\\s+$", "").split(" ");

        int s = Integer.parseInt(firstMultipleInput[0]);

        int t = Integer.parseInt(firstMultipleInput[1]);

        String[] secondMultipleInput = bufferedReader.readLine().replaceAll("\\s+$", "").split(" ");

        int a = Integer.parseInt(secondMultipleInput[0]);

        int b = Integer.parseInt(secondMultipleInput[1]);

        String[] thirdMultipleInput = bufferedReader.readLine().replaceAll("\\s+$", "").split(" ");

        int m = Integer.parseInt(thirdMultipleInput[0]);

        int n = Integer.parseInt(thirdMultipleInput[1]);

        List<Integer> apples = Stream.of(bufferedReader.readLine().replaceAll("\\s+$", "").split(" "))
            .map(Integer::parseInt)
            .collect(toList());

        List<Integer> oranges = Stream.of(bufferedReader.readLine().replaceAll("\\s+$", "").split(" "))
            .map(Integer::parseInt)
            .collect(toList());

        Result.countApplesAndOranges(s, t, a, b, apples, oranges);

        bufferedReader.close();
    }
}

#Birthday cake candles

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
     * Complete the 'birthdayCakeCandles' function below.
     *
     * The function is expected to return an INTEGER.
     * The function accepts INTEGER_ARRAY candles as parameter.
     */

    public static int birthdayCakeCandles(List<Integer> candles) {
        int largest=candles.get(0);
        int tot=0;
        for (int i = 1; i < candles.size(); i++) {
            if(largest<candles.get(i)){
                largest=candles.get(i);
            }
        }
        for (int j = 0; j < candles.size(); j++) {
            if(largest==candles.get(j)){
                tot++;
            }
            
        }
        
        
        return tot;

    }

}

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter bufferedWriter = new BufferedWriter(new FileWriter(System.getenv("OUTPUT_PATH")));

        int candlesCount = Integer.parseInt(bufferedReader.readLine().trim());

        List<Integer> candles = Stream.of(bufferedReader.readLine().replaceAll("\\s+$", "").split(" "))
            .map(Integer::parseInt)
            .collect(toList());

        int result = Result.birthdayCakeCandles(candles);

        bufferedWriter.write(String.valueOf(result));
        bufferedWriter.newLine();

        bufferedReader.close();
        bufferedWriter.close();
    }
}

#Grading students
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
     * Complete the 'gradingStudents' function below.
     *
     * The function is expected to return an INTEGER_ARRAY.
     * The function accepts INTEGER_ARRAY grades as parameter.
     */

    public static List<Integer> gradingStudents(List<Integer> grades) {
           List<Integer> orggrade=new ArrayList<Integer>();
    for (int i = 0; i < grades.size(); i++) {
        int arr=grades.get(i);

        if(grades.get(i)>=38){
            if(arr%5==0){
                 orggrade.add(arr);

            }else{
            int rounded=((arr/5)+1)*5;
            if(rounded-arr<3){
                orggrade.add(rounded);
            }else{
                orggrade.add(arr);

            }
            }
            }else{
                orggrade.add(arr);

            }
        }
                    return orggrade;

    }

    }


public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter bufferedWriter = new BufferedWriter(new FileWriter(System.getenv("OUTPUT_PATH")));

        int gradesCount = Integer.parseInt(bufferedReader.readLine().trim());

        List<Integer> grades = IntStream.range(0, gradesCount).mapToObj(i -> {
            try {
                return bufferedReader.readLine().replaceAll("\\s+$", "");
            } catch (IOException ex) {
                throw new RuntimeException(ex);
            }
        })
            .map(String::trim)
            .map(Integer::parseInt)
            .collect(toList());

        List<Integer> result = Result.gradingStudents(grades);

        bufferedWriter.write(
            result.stream()
                .map(Object::toString)
                .collect(joining("\n"))
            + "\n"
        );

        bufferedReader.close();
        bufferedWriter.close();
    }
}

#min max sum

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
