```java
class Main {

    static void pairssum(int a[],
                        int size, int sum)
    {
        //traverse through the array to find pairs
        for (int i = 0; i < size; i++)
            for (int j = i + 1; j < size; j++)
                if (a[i] + a[j] == sum)
                    System.out.println(“(“ + a[i] + “, “ + a[j] + “)”);
    }

    // Driver Code
    
    public static void main(String[] arg)
    {
        int a[] = { 2, 4, 6, 8, 10 };
        int size = a.length;
        int sum = 10;
        pairssum(a, size, sum);
    }
}
```
