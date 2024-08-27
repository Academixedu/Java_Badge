## Introduction

### Welcome to Java!
```java
public class Solution {

    public static void main(String[] args) {
      System.out.println("Hello, World.");
      System.out.println("Hello, Java.");
    }
}
```
### Java IF-Else
```java
import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.regex.*;

public class Solution {



    private static final Scanner scanner = new Scanner(System.in);

    public static void main(String[] args) {
        int N = scanner.nextInt();
        scanner.skip("(\r\n|[\n\r\u2028\u2029\u0085])?");
if(N%2!=0){
    System.out.println("Weird");
}
if(N%2==0&&(N<=5&&N>=2)){
    System.out.println("Not Weird");
}
if(N%2==0&&(N>=6&&N<=20)){
    System.out.println("Weird");
}
if(N%2==0&&(N>20)){
    System.out.println("Not Weird");
}
        scanner.close();
    }
}
```
### Java Stdin and Stdout II
```java
import java.util.Scanner;

public class Solution {

    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        int i = scan.nextInt();
        Double d=scan.nextDouble();
        scan.nextLine();
        String s=scan.nextLine();
        System.out.println("String: " + s);
        System.out.println("Double: " + d);
        System.out.println("Int: " + i);
    }
}
```
### Java Output Formatting
```java
import java.util.Scanner;

public class Solution {

    public static void main(String[] args) {
            Scanner sc=new Scanner(System.in);
            System.out.println("================================");
            
            for(int i=0;i<3;i++){
                String s1=sc.next();
                int x=sc.nextInt();
                int count=0;
                int temp=x;
                
                if (x == 0) {
                count = 1;
            } else {
          
                while (temp != 0) {
          
                    temp = temp / 10;
                    count++;
                }
            }
                
                System.out.print(s1);
         
      
                for(int j=s1.length();j<15;j++){
                    System.out.print(" ");
                }

                for(int j=1;j<=3-count;j++){
                    System.out.print("0");
                }
                System.out.println(x);
            }
            
            System.out.println("================================");

    }
}
```
### LOOPS 1
```java
import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.regex.*;



public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));

        int N = Integer.parseInt(bufferedReader.readLine().trim());
for(int i=1;i<=10;i++){
    System.out.println(N+" x "+i+" = "+N*i);
}
        bufferedReader.close();
    }
}
```
### Loops 2
```java
import java.util.*;
import java.io.*;

class Solution{
    public static void main(String []argh){
        Scanner in = new Scanner(System.in);
        int t=in.nextInt();
        for(int i=0;i<t;i++){
            int a=in.nextInt();
            int b=in.nextInt();
            int c=in.nextInt();
            int mul=1;
            for(int j=0;j<c;j++){
              
                System.out.print((a=a+mul*b)+" ");
                mul=mul*2;
             
                            }
            System.out.println();
        }
           in.close();
    }
}
```
### DataTypes
```java
import java.util.*;
import java.io.*;



class Solution{
    public static void main(String []argh)
    {



        Scanner sc = new Scanner(System.in);
        int t=sc.nextInt();

        for(int i=0;i<t;i++)
        {

            try
            {
                long x=sc.nextLong();
                System.out.println(x+" can be fitted in:");
                if(x>=-128 && x<=127)System.out.println("* byte");
                if(x>=Short.MIN_VALUE&&x<=Short.MAX_VALUE){
                    System.out.println("* short");
                }
                if(x>=Integer.MIN_VALUE&&x<=Integer.MAX_VALUE){
                    System.out.println("* int");
                }
                if(x>=Long.MIN_VALUE&&x<=Long.MAX_VALUE)System.out.println("* long");
            }
            catch(Exception e)
            {
                System.out.println(sc.next()+" can't be fitted anywhere.");
            }

        }
    }
}
```
### End-of-File
```java
import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;

public class Solution {

    public static void main(String[] args) {
    Scanner in=new Scanner(System.in);
    int lineno=1;
     while(in.hasNext()){
    String txt=in.nextLine();
    System.out.println(lineno+" "+txt);
    lineno++;
      }
      in.close();
    }
}
```
### Static Initializer Block
```java
import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;

public class Solution {

static int B; 
static int H;   
static boolean flag;

static {
Scanner in=new Scanner(System.in);
B=in.nextInt();
H=in.nextInt();
if(B>0&&H>0){
    flag=true;
}
else{
    System.out.println("java.lang.Exception: Breadth and height must be positive");
}
in.close();
}

public static void main(String[] args){
		if(flag){
			int area=B*H;
			System.out.print(area);
		}
		
	}//end of main

}//end of class

```
### Java Int to String
```java
import java.util.*;
import java.security.*;
public class Solution {
 public static void main(String[] args) {

  DoNotTerminate.forbidExit();

  try {
   Scanner in = new Scanner(System.in);
   int n = in .nextInt();
   in.close();
   //String s=???; Complete this line below
String s=Integer.toString(n);
   //Write your code here

   
   if (n == Integer.parseInt(s)) {
    System.out.println("Good job");
   } else {
    System.out.println("Wrong answer.");
   }
  } catch (DoNotTerminate.ExitTrappedException e) {
   System.out.println("Unsuccessful Termination!!");
  }
 }
}

//The following class will prevent you from terminating the code using exit(0)!
class DoNotTerminate {

 public static class ExitTrappedException extends SecurityException {

  private static final long serialVersionUID = 1;
 }

 public static void forbidExit() {
  final SecurityManager securityManager = new SecurityManager() {
   @Override
   public void checkPermission(Permission permission) {
    if (permission.getName().contains("exitVM")) {
     throw new ExitTrappedException();
    }
   }
  };
  System.setSecurityManager(securityManager);
 }
}
```
### Java Date and Time
```java
import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.regex.*;

class Result {

    /*
     * Complete the 'findDay' function below.
     *
     * The function is expected to return a STRING.
     * The function accepts following parameters:
     *  1. INTEGER month
     *  2. INTEGER day
     *  3. INTEGER year
     */

    public static String findDay(int month, int day, int year) {
     
        Calendar calendar = Calendar.getInstance();
        calendar.set(year, month - 1, day); 
        int dayOfWeek = calendar.get(Calendar.DAY_OF_WEEK);

  String[] days = { "SUNDAY", "MONDAY", "TUESDAY", "WEDNESDAY", "THURSDAY", "FRIDAY", "SATURDAY" };
        
        return days[dayOfWeek - 1];   
    }

}

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter bufferedWriter = new BufferedWriter(new FileWriter(System.getenv("OUTPUT_PATH")));

        String[] firstMultipleInput = bufferedReader.readLine().replaceAll("\\s+$", "").split(" ");

        int month = Integer.parseInt(firstMultipleInput[0]);

        int day = Integer.parseInt(firstMultipleInput[1]);

        int year = Integer.parseInt(firstMultipleInput[2]);

        String res = Result.findDay(month, day, year);

        bufferedWriter.write(res);
        bufferedWriter.newLine();

        bufferedReader.close();
        bufferedWriter.close();
    }
}
```
### Currency Formatter
```java
import java.util.*;
import java.text.*;

public class Solution {
    
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        double payment = scanner.nextDouble();
        scanner.close();
        
        // Create NumberFormat instances for each locale
        NumberFormat usFormat = NumberFormat.getCurrencyInstance(Locale.US);
        NumberFormat indiaFormat = NumberFormat.getCurrencyInstance(new Locale("en", "IN"));
        NumberFormat chinaFormat = NumberFormat.getCurrencyInstance(Locale.CHINA);
        NumberFormat franceFormat = NumberFormat.getCurrencyInstance(Locale.FRANCE);
        
        // Format the payment value according to each locale
        String us = usFormat.format(payment);
        String india = indiaFormat.format(payment);
        String china = chinaFormat.format(payment);
        String france = franceFormat.format(payment);
        
        // Print the formatted values
        System.out.println("US: " + us);
        System.out.println("India: " + india);
        System.out.println("China: " + china);
        System.out.println("France: " + france);
    }
}
```
## Strings

### String Introduction
```java
import java.io.*;
import java.util.*;

public class Solution {

    public static void main(String[] args) {
        
        Scanner sc=new Scanner(System.in);
        String A=sc.next();
        String B=sc.next();
        System.out.println(A.length()+B.length());
        if(A.compareTo(B)>0){
            System.out.println("Yes");
        }
        else{
            System.out.println("No");
        }
        String Hello=A.substring(0, 1).toUpperCase()+A.substring(1);
        String Java=B.substring(0, 1).toUpperCase()+B.substring(1);
        System.out.println(Hello+" "+Java);
        
    }
}
```









