# Java 中的前 30 种模式:如何打印星号、数字和字符

> 原文：<https://www.edureka.co/blog/30-pattern-programs-in-java/>

**[Java 面试](https://www.edureka.co/blog/interview-questions/java-interview-questions/)** 会让程序员不好过，这就是过程的严重性。参加过这个过程的人都会知道，在 **[程序](https://www.edureka.co/blog/java-programs/)** 列表中应该会弹出一个模式程序。这篇文章重点关注 Java 中的模式程序。我将这些项目分为以下几组:

## **Java 中的模式程序**

*   [Java 中的星型模式](#starpatterninjava)
*   [数字模式](#numericpatterns)
*   [字符模式](#characterpattern)

让我们开始吧。:-)

## **Java 中的星型模式**

首先，让我们从 **[Java](https://www.edureka.co/blog/java-tutorial/)** 即金字塔中的基本和常见的模式程序开始。

### **1。金字塔计划**

```
    * 
   * * 
  * * * 
 * * * * 
* * * * *
```

让我们编写 java 代码来更好地理解这种模式。

```
public class Edureka
{  
    public static void pyramidPattern(int n) 
    {  
        for (int i=0; i<n; i++) //outer loop for number of rows(n) { for (int j=n-i; j>1; j--) //inner loop for spaces
            { 
                System.out.print(" "); //print space
            }  
            for (int j=0; j<=i; j++ ) //inner loop for number of columns
            { 
                System.out.print("* "); //print star
            } 

            System.out.println(); //ending line after each row
        } 
    } 

    public static void main(String args[]) //driver function
    { 
        int n = 5; 
        pyramidPattern(n); 
    } 
}
```

### **2。直角三角形星形图案**

** ** * ** * ** * * * * *

```
public class Edureka 
{ 
    public static void rightTriangle(int n) 
    { 
        int i, j;  
        for(i=0; i<n; i++) //outer loop for number of rows(n) { for(j=2*(n-i); j>=0; j--) // inner loop for spaces 
            {           
                System.out.print(" "); // printing space
            } 
            for(j=0; j<=i; j++) //  inner loop for columns
            {       
                System.out.print("* "); // print star
            }           
            System.out.println(); // ending line after each row
        } 
    } 
    public static void main(String args[]) 
    { 
        int n = 5; 
        rightTriangle(n); 
    } 
}
```

**3。左三角星形图案**

```
           * 
         * * 
       * * * 
     * * * * 
   * * * * * 

```

```
public class Edureka 
{ 
    public static void printStars(int n) 
    { 
        int i, j;  
        for(i=0; i<n; i++) //outer loop for number of rows(n) { for(j=2*(n-i); j>=0; j--) // inner loop for spaces 
            {           
                System.out.print(" "); // printing space
            } 
            for(j=0; j<=i; j++) //  inner loop for columns
            {       
                System.out.print("* "); // print star
            }           
            System.out.println(); // ending line after each row
        } 
    } 
    public static void main(String args[]) 
    { 
        int n = 5; 
        printStars(n); 
    } 
}

```

### **4。Java 中的菱形图案程序**

输入行数:5

```
    *
   ***
  *****
 *******
*********
 *******
  *****
   ***
    *

```

```
import java.util.Scanner;
public class Edureka
{
public static void main(String args[])
{
int n, i, j, space = 1;
System.out.print("Enter the number of rows: ");
Scanner s = new Scanner(System.in);
n = s.nextInt();
space = n - 1;
for (j = 1; j<= n; j++)
{
for (i = 1; i<= space; i++)
{
System.out.print(" ");
}
space--;
for (i = 1; i <= 2 * j - 1; i++)
{
System.out.print("*");
}
System.out.println("");
}
space = 1;
for (j = 1; j<= n - 1; j++)
{
for (i = 1; i<= space; i++)
{
System.out.print(" ");
}
space++;
for (i = 1; i<= 2 * (n - j) - 1; i++)
{
System.out.print("*");
}
System.out.println("");
}
}
}
```

### **5。向下的三角形星形图案**

输入行数:5

```
* * * * * 
* * * * 
* * * 
* * 
* 

```

```

import java.util.Scanner;
public class Edureka
{
	public static void main(String[] args)
	{
	Scanner sc = new Scanner(System.in);

	System.out.println("Enter the number of rows: "); //takes input from user

	int rows = sc.nextInt();

	for (int i= rows-1; i>=0 ; i--)
	{
	for (int j=0; j<=i; j++)
	{
	System.out.print("*" + " ");
	}
	System.out.println();
	}
	sc.close();
	}
	} 
```

### **6。镜像直角三角形星形程序**

输入行数:5

```
     *
    **
   ***
  ****
 *****
******

```

```

import java.util.Scanner;
public class Edureka
{
	public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);

        System.out.println("Enter number of rows: "); // takes input from user

        int rows = sc.nextInt();

        for (int i= 0; i<= rows; i++)
        {
            for (int j=1; j<=rows-i; j++)
            {
                System.out.print(" ");
            }
            for (int k=0;k<=i;k++)
            {
                System.out.print("*");
            } 
                System.out.println("");
        }
        sc.close();

    }
}

```

### ****7。倒金字塔星形图案****

输入行数:5

```
 * * * * * 
  * * * * 
   * * * 
    * * 
     * 

```

```
import java.util.Scanner;
public class Edureka
{
	public static void main(String[] args)
{
    Scanner sc = new Scanner(System.in);
    System.out.println("Enter the number of rows: ");

    int rows = sc.nextInt();        
    for (int i= 0; i<= rows-1 ; i++)
    {
        for (int j=0; j<=i; j++)
        {
            System.out.print(" ");
        }
        for (int k=0; k<=rows-1-i; k++)
        {
            System.out.print("*" + " ");
        }
        System.out.println();
    }
    sc.close();

}
}

```

**8。右下镜像星形图案** 输入行数:5

```
*****
 ****
  ***
   **
    *

```

```

import java.util.Scanner;
public class Edureka
{

	public static void main(String[] args)
	{
	Scanner sc = new Scanner(System.in); // takes input
	System.out.println("Enter number of rows: ");
	int rows = sc.nextInt();
	for (int i= rows; i>= 1; i--)
	{
	for (int j=rows; j>i;j--)
	{
	System.out.print(" ");
	}
	for (int k=1;k<=i;k++)
	{
	System.out.print("*");
	}
	System.out.println("");
	}
	sc.close();
	}
	}

```

### **9。右帕斯卡三角形**

输入行数:5

```
* 
* * 
* * * 
* * * * 
* * * * * 
* * * * 
* * * 
* * 
* 

```

```

import java.util.Scanner;
public class Edureka
{
	public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the number of rows: ");

        int rows = sc.nextInt();        
        for (int i= 0; i<= rows-1 ; i++)
        {
            for (int j=0; j<=i; j++) { System.out.print("*"+ " "); } System.out.println(""); } for (int i=rows-1; i>=0; i--)
        {
            for(int j=0; j <= i-1;j++)
            {
                System.out.print("*"+ " ");
            }
            System.out.println("");
        }
        sc.close();
    }
}

```

### 10。左三角帕斯卡的

输入行数:5

```
    *
   **
  ***
 ****
*****
 ****
  ***
   **
    *

```

```
import java.util.Scanner;
public class Edureka
{

	public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the number of rows: ");

        int rows = sc.nextInt();        
        for (int i= 1; i<= rows ; i++)
        {
            for (int j=i; j <rows ;j++)            
        {
                System.out.print(" ");
            }
            for (int k=1; k<=i;k++) { System.out.print("*"); } System.out.println(""); } for (int i=rows; i>=1; i--)
        {
            for(int j=i; j<=rows;j++)
            {
                System.out.print(" ");
            }
            for(int k=1; k<i ;k++) 
            {
                System.out.print("*");
            }
            System.out.println("");

        }
        sc.close();
    }
}

```

### **11。沙漏星形图案**

输入行数:5

```
* * * * * 
 * * * * 
  * * * 
   * * 
    * 
    * 
   * * 
  * * * 
 * * * * 
* * * * * 

```

```
import java.util.Scanner;
public class Edureka
{
	public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the number of rows: ");

        int rows = sc.nextInt();	        
        for (int i= 0; i<= rows-1 ; i++)
        {
            for (int j=0; j <i; j++)
            {
                System.out.print(" ");
            }
            for (int k=i; k<=rows-1; k++) { System.out.print("*" + " "); } System.out.println(""); } for (int i= rows-1; i>= 0; i--)
        {
            for (int j=0; j< i ;j++)
            {
                System.out.print(" ");
            }
            for (int k=i; k<=rows-1; k++)
            {
                System.out.print("*" + " ");
            }
            System.out.println("");
        }
        sc.close();
    }
}

```

### **12。字母 A 模式**

```
** 
* *
***
* *
* *
* *
```

```
import java.util.Scanner;
public class Edureka
{
	// Java program to print alphabet A pattern
	void display(int n)
	{
	// Outer for loop for number of lines
	for (int i = 0; i<=n; i++) {
	// Inner for loop for logic execution
	for (int j = 0; j<= n / 2; j++) {
	// prints two column lines
	if ((j == 0 || j == n / 2) && i != 0 ||
	// print first line of alphabet
	i == 0  && j != n / 2 ||
	// prints middle line
	i == n / 2)
	System.out.print("*");
	else
	System.out.print(" ");
	}
	System.out.println();
	}
	}
	public static void main(String[] args)
	{
	Scanner sc = new Scanner(System.in);
	Edureka a = new Edureka();
	a.display(7);
	}
	}
```

### 13。三角形星形图案

输入行数:5

```
    *
   * *
  *   *
 *     *
*********

```

```

import java.util.Scanner;
public class Edureka
{
	 public static void main(String[] args)
	    {
	        Scanner sc = new Scanner(System.in);

	        System.out.println("Enter the number of rows: ");

	        int rows = sc.nextInt();

	        for (int i=1; i<= rows ; i++)
	        {
	            for (int j = i; j < rows ; j++) {
	                System.out.print(" ");
	            }   
	            for (int k = 1; k <= (2*i -1) ;k++) {
	                if( k==1 || i == rows || k==(2*i-1)) {
	                    System.out.print("*");
	                }
	                else {
	                    System.out.print(" ");
	                }
	            }
	            System.out.println("");
	        }
	        sc.close();
	    }
	}

```

### **14。向下三角形**

输入行数:5

```
*********
 *     *
  *   *
   * *
    *

```

```

import java.util.Scanner;
public class Edureka
{
public static void main(String[] args)
{
    Scanner sc = new Scanner(System.in);
    System.out.println("Enter the number of rows: ");

    int rows = sc.nextInt();    
     for (int i=rows; i>= 1 ; i--)
    {
        for (int j = i; j < rows ; j++) {
            System.out.print(" ");
        }   
        for (int k = 1; k <= (2*i -1) ;k++) {
            if( k==1 || i == rows || k==(2*i-1)) {
                System.out.print("*");
            }
            else {
                System.out.print(" ");
            }
        }
        System.out.println("");
    }
    sc.close();
}
}

```

### 15。菱形星形图案

输入行数:5

```
    *
   * *
  *   *
 *     *
*       *
 *     *
  *   *
   * *
    *

```

```
import java.util.Scanner;
public class Edureka
{
	public static void main(String[] args)
{
    Scanner sc = new Scanner(System.in);

    System.out.println("Enter the number of rows: ");

    int rows = sc.nextInt();    
    for (int i=1; i<= rows ; i++) { for (int j = rows; j > i ; j--) {
            System.out.print(" ");
        }
        System.out.print("*");
        for (int k = 1; k < 2*(i -1) ;k++) { System.out.print(" "); } if( i==1) { System.out.println(""); } else { System.out.println("*"); } } for (int i=rows-1; i>= 1 ; i--)
        {
        for (int j = rows; j > i ; j--) {
            System.out.print(" ");
        }
        System.out.print("*");
        for (int k = 1; k < 2*(i -1) ;k++) {
            System.out.print(" ");
        }
        if( i==1)
            System.out.println("");
        else
            System.out.println("*");
    }
    sc.close();
}
}

```

现在我们已经用 [Java](https://www.edureka.co/blog/what-is-java/) 实现了星型模式程序。让我们更进一步，实现一些数字模式。

## **Java 中的数字模式**

### **1。简单数字程序**

```
1 
1 2 
1 2 3 
1 2 3 4 
1 2 3 4 5
```

```

public class Edureka
{
	public static void printNums(int n) 
    { 
        int i, j,num; 

        for(i=0; i<n; i++) // outer loop for rows
        { 
            num=1; 
            for(j=0; j<=i; j++) // inner loop for rows
            { 
                // printing num with a space  
                System.out.print(num+ " "); 

                //incrementing value of num 
                num++; 
            } 

            // ending line after each row 
            System.out.println(); 
        } 
    } 
       public static void main(String args[]) 
    { 
        int n = 5; 
        printNums(n); 
    } 
}

```

### **2。java 中的数字模式程序**

```
1 
2 3 
4 5 6 
7 8 9 10 
11 12 13 14 15 

```

```
import java.util.Scanner;

public class Edureka
{            
        public static void main(String[] args) {
            int i, j, k = 1;
            for (i = 1; i <= 5; i++) {
                for (j = 1; j< i + 1; j++) {
                    System.out.print(k++ + " ");
                }

                System.out.println();
            }
        }

    }

```

### **3。Java 中的帕斯卡三角程序**

```
             1
           1   1
         1   2   1
       1   3   3   1
     1   4   6   4   1

```

```

import java.util.Scanner;

public class Edureka
{			 
	public static void main(String[] args) {

        int n = 5;

        for (int i = 0; i < n; i++) {
            int number = 1;
            System.out.printf("%" + (n - i) * 2 + "s", "");
            for (int j = 0; j <= i; j++) {
                System.out.printf("%4d", number);
                number = number * (i - j) / (j + 1);
            }
            System.out.println();
        }

    }

}

```

### **4。Java 中的菱形图案程序**

```
   1
  212
 32123
4321234
 32123
  212
   1

```

```
import java.util.Scanner;

public class Edureka
{            
    public static void main(String[] args) {
        for (int i = 1; i <= 4; i++)
        {
            int n = 4;

            for (int j = 1; j<= n - i; j++) { System.out.print(" "); } for (int k = i; k >= 1; k--)
            {
                System.out.print(k);
            }
            for (int l = 2; l <= i; l++) { System.out.print(l); } System.out.println(); } for (int i = 3; i >= 1; i--)
        {
            int n = 3;

            for (int j = 0; j<= n - i; j++) { System.out.print(" "); } for (int k = i; k >= 1; k--)
            {
                System.out.print(k);
            }
            for (int l = 2; l <= i; l++)
            {
                System.out.print(l);
            }

            System.out.println();
        }

    }
}

```

### **5。Java 中的数字模式程序**

输入行数:5

```
1 
2 2 
3 3 3 
4 4 4 4 
5 5 5 5 5
```

```

import java.util.Scanner;

public class Edureka
{            
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in); //Taking rows value from the user    
        System.out.println("Enter the number of rows: ");    
        int rows = sc.nextInt();         
        for (int i = 1; i <= rows; i++) 
        {
            for (int j = 1; j <= i; j++)
            {
                System.out.print(i+" ");
            }

            System.out.println();
        }         
        sc.close();
    }
}

```

### **6。降序排列模式**

输入行数:5

```
5 
5 4 
5 4 3 
5 4 3 2 
5 4 3 2 1
```

```
import java.util.Scanner;
public class Edureka
{
public static void main(String[] args)
{
Scanner sc = new Scanner(System.in);

//Taking rows value from the user

System.out.println("Enter the number of rows: ");

int rows = sc.nextInt();
for (int i = rows; i >= 1; i--)
{
for (int j = rows; j >= i; j--)
{
System.out.print(j+" ");
}

System.out.println();
}
sc.close();
}
}

```

### **7。直角三角形数字图案**

输入行数:5

```
1 
2 1 
3 2 1 
4 3 2 1 
5 4 3 2 1
```

```

import java.util.Scanner;
public class Edureka
{

public static void main(String[] args) 
{
Scanner sc = new Scanner(System.in);

System.out.println("Enter the number of rows: ");

int rows = sc.nextInt();

for (int i = 1; i <= rows; i++) { for (int j = i; j >= 1; j--)
   {
       System.out.print(j+" ");
   }

   System.out.println();
}         
sc.close();
}
}

```

### **8。二进制数字模式**

输入行数:5

```
10101
01010
10101
01010
10101
```

```

import java.util.Scanner;
public class Edureka
{

	public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);

        System.out.println("Enter the number of rows: ");

        int rows = sc.nextInt();

        for (int i = 1; i <= rows; i++) 
        {
            int num;

            if(i%2 == 0)
            {
                num = 0;

                for (int j = 1; j <= rows; j++)
                {
                    System.out.print(num);

                    num = (num == 0)? 1 : 0;
                }
            }
            else
            {
                num = 1;

                for (int j = 1; j <= rows; j++)
                {
                    System.out.print(num);

                    num = (num == 0)? 1 : 0;
                }
            }

            System.out.println();
        }

        sc.close();
    }
}			 

```

### **9。0/1 模式程序**

输入行数:5

```
1
10
101
1010
10101
```

```

import java.util.Scanner;

public class Edureka
{			 
	public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);

        System.out.println("Enter the number of rows: ");

        int rows = sc.nextInt();         
        for (int i = 1; i <= rows; i++) 
        {
            for (int j = 1; j <= i; j++)
            {
                if(j%2 == 0)
                {
                    System.out.print(0);
                }
                else
                {
                    System.out.print(1);
                }
            }

            System.out.println();
        }

        sc.close();
    }
}

```

### **10。菱形数字图案**

```
1 2 3 4 5 
 2 3 4 5 
  3 4 5 
   4 5 
    5 
   4 5 
  3 4 5 
 2 3 4 5 
1 2 3 4 5
```

```
import java.util.Scanner;
public class Edureka
{
	public static void main(String[] args) 
    {

        int n = 5;  

        for (int i = 1; i <= n; i++) 
        {
            for (int j = 1; j < i; j++) 
            {
                System.out.print(" ");
            }

            for (int k = i; k <= n; k++) { System.out.print(k+" "); } System.out.println(); } for (int i = n-1; i >= 1; i--) 
        {
             for (int j = 1; j < i; j++) 
            {
                System.out.print(" ");
            }
            for (int k = i; k <= n; k++)
            {
                System.out.print(k+" ");
            }

            System.out.println();
        }

    }
}

```

现在我们已经用 Java 实现了数字模式[程序。让我们更进一步，实现一些字符/字母模式。](https://www.edureka.co/blog/java-programs/)

## **Java 中的字母/字符模式**

### **1。右字母三角形**

```
A 
A B 
A B C 
A B C D 
A B C D E 
A B C D E F
```

```

import java.util.Scanner;

public class Edureka
{			 
	public static void main(String[] args)
    {
        int alphabet = 65;
                for (int i = 0; i <= 5; i++)
        {
            for (int j = 0; j <= i; j++)
            {
                System.out.print((char) (alphabet + j) + " ");
            }
            System.out.println();
        }
    }
}

```

### **2。字母/字符模式程序**

```
A 
B B 
C C C 
D D D D 
E E E E E 
F F F F F F 

```

```

import java.util.Scanner;

public class Edureka
{			 
	public static void main(String[] args)
    {
        int alphabet = 65;
                for (int i = 0; i<= 5; i++)
        {
            for (int j = 0; j <= i; j++)
            {
                System.out.print((char) alphabet + " ");
            }
            alphabet++;
            System.out.println();
        }
    }
}

```

### **3。k 形字符模式程序**

```
A B C D E F 
A B C D E 
A B C D 
A B C 
A B 
A 
A 
A B 
A B C 
A B C D 
A B C D E 
A B C D E F
```

```

import java.util.Scanner;

public class Edureka
{public static void main(String[] args)
{
for (int i = 5; i >= 0; i--)
{
   int alphabet = 65;
   for (int j = 0; j <= i; j++)
   {
       System.out.print((char) (alphabet + j) + " ");
   }
   System.out.println();
}
for (int i = 0; i<= 5; i++)
{
   int alphabet = 65;
   for (int j = 0; j <= i; j++)
   {
       System.out.print((char) (alphabet + j) + " ");
   }
   System.out.println();
}
}
}

```

### **4。Java 中的三角字符模式程序**

```
     A 
    A B 
   A B C 
  A B C D 
 A B C D E 
A B C D E F
```

```

public class Edureka
{			 
	public static void main(String[] args)
{
		for (int i = 0; i <= 5; i++) { int alphabet = 65; for (int j = 5; j > i; j--)
        {
            System.out.print(" ");
        }
        for (int k = 0; k <= i; k++)
        {
            System.out.print((char) (alphabet + k) + " ");
        }
        System.out.println();
    }
}
}

```

### **5。Java 中的菱形模式**

输入 A 到 Z : F 之间的字符

```
     A
    B B
   C   C
  D     D
 E       E
F         F
 E       E
  D     D
   C   C
    B B
     A
```

```
import java.util.Scanner;

public class Edureka
{public static void main(String[] args) {
    char[] letter = { 'A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J',
            'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V',
            'W', 'X', 'Y', 'Z' };
    int letter_number = 0;
    String[] diamond = new String[26]; // array of strings
    System.out.print("Enter a Character between A to Z : ");

    Scanner reader = new Scanner(System.in);
    try {
        char user_letter = reader.next("[A-Z]").charAt(0);
        // search for letter number in the array letter
        for (int i = 0; i < letter.length; i++) {
            if (letter[i] == user_letter) {
                letter_number = i;
                break;
            }
        }

        // construct diamond
        for (int i = 0; i <= letter_number; i++) {
            diamond[i] = "";
            // add initial spaces
            for (int j = 0; j < letter_number - i; j++) {
                diamond[i] += " ";
            }

            // add letter
            diamond[i] += letter[i];

            // add space between letters
            if (letter[i] != 'A') {
                for (int j = 0; j < 2 * i - 1; j++) { diamond[i] += " "; } // add letter diamond[i] += letter[i]; } // Draw the first part of the diamond System.out.println(diamond[i]); } for (int i = letter_number - 1; i >= 0; i--)
				{
            // Draw the second part of the diamond
            // Writing the diamondArray in reverse order
            System.out.println(diamond[i]);
        }
    } catch (Exception e) {
        e.printStackTrace();
    } finally {
        reader.close();
    }

}
}

```

这就把我们带到了 java 博客中前 30 名模式程序的结尾。我希望你觉得它很有启发性，并帮助你理解了 [Java 基础知识](https://www.edureka.co/blog/java-tutorial/)。如果您刚刚开始，那么请阅读这篇 Java 教程，了解基本的 Java 概念。

[https://www.youtube.com/embed/aqHhpahguVY](https://www.youtube.com/embed/aqHhpahguVY)

*查看 Edureka 的 **[Java 培训](https://www.edureka.co/java-j2ee-training-course)** ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。我们在这里帮助你的旅程中的每一步，为了成为一个除了这个 java 面试问题，我们提出了一个课程，这是为学生和专业人士谁想要成为一个 Java 开发人员设计的。该课程旨在为您提供 Java 编程的开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*

*有问题吗？请在这篇“Java* 模式程序”文章*的评论部分提到它，我们会尽快回复您，或者您也可以参加我们在 Amravati 的 [Java 培训。](https://www.edureka.co/java-j2ee-training-course-amravati)*