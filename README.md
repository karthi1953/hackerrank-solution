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
            }catch(Exception e){
                  System.out.println("Invalid");

            }
        }

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
