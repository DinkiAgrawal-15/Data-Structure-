```java
package Recursion;
import java.util.Scanner;

public class BinarySearch {

	public static void main(String[] args) {		
		Scanner sc = new Scanner(System.in);
		System.out.print("Enter the no . of elements to be entered in the array : ");
		int n = sc.nextInt();
		System.out.print("Enter the elements into the array : ");
		int a[] = new int[n];
		for(int i = 0 ; i < n ; i++)
		
		{
			a[i] = sc.nextInt();
		}
		System.out.print("Enter the element to be searched in the array : ");
		int ele = sc.nextInt();
		BS(a , ele);
		sc.close();

	}
	public static void BS(int a[] , int ele)
	{
		int l = 0 , r = (a.length) - 1 ;
		int mid ;
		while(l < r)
		{
			mid = (l + r) / 2 ;
			if(ele == a[mid])
			{
				 System.out.println("Element found at index : "+mid);
				 break ;
			}
			else if(ele < a[mid])
			{
				r = mid - 1 ;
			}
			else
			{
				l = mid + 1 ;
			}
		}
		if(l > r)
		{
			System.out.println("Element not found!!.");
		}
	}
}
```
