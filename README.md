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
