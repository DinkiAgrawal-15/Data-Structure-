```java
import java.util.*; 
class Main 
{ 
    // A  method to swap two numbers. 
    void swap(int arr[], int a, int b) 
    { 
        int temp = arr[a]; 
        arr[a] = arr[b]; 
        arr[b] = temp; 
    } 

    
    
    void sortwave(int arr[], int n) 
    { 
        // Sort the input array 
        Arrays.sort(arr); 

        // Swap adjacent elements 
        for (int i=0; i<n-1; i += 2) 
            swap(arr, i, i+1); 
    } 

    // Driver method 
    public static void main(String args[]) 
    { 
        prepinsta p = new prepinsta(); 
        int arr[] = {10, 90, 49, 2, 1, 5, 23}; 
        int n = arr.length; 
        p.sortwave(arr, n); 
        for (int i : arr) 
            System.out.print(i + ” “); 
    } 
} 
```
