```java
import java.util.Scanner;

public class Main {

	public static void main(String[] args) {
		int i,num,item,a[];
		Scanner sc = new Scanner(System.in);
		System.out.println("Enter the number of element you want to insert");
		num=sc.nextInt();
		a=new int[num];
		System.out.println("Enter the elements in array");
		for(i=0;i<num;i++){
		    a[i]=sc.nextInt();
		    
		}
		System.out.println("Enter the element to be search");
		item=sc.nextInt();
		for(i=0;i<num;i++){
		    if(a[i]==item){
		        System.out.println(item+"is present in the index"+(i+1));
		        break;
		    }
		    }
	}
		}
		
    
    ---------------------------------------------------------
    Enter the number of element you want to insert
5
Enter the elements in array
2 3 6 8 4
Enter the element to be search
8
is present in the index4
```
