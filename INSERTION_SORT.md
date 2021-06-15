```java
import java.util.*;
class Main
	{
   public static void main(String args[]) 
    { 
        int a[] = { 12,11,13,5,6 };

        PrepInsta ob = new PrepInsta(); 
        ob.sort(a); 

        printArray(a); 
    }
    void sort(int a[]) 
    { 
        int len = a.length;
        for (int i = 1; i < len; i++) 
	   { 
            int key = a[i]; 
            int j = i - 1; 
            while (j >= 0 && a[j] > key) 
				{ 
                  a[j + 1] = a[j]; 
                  j = j - 1; 
                } 
                   a[j + 1] = key; 
            } 
    } 

    static void printArray(int a[]) 
    { 
        int len = a.length; 
        for (int i = 0; i < len; ++i) 
            System.out.print(a[i] + " "); 
            System.out.println(); 
    } 
  }
```
