# Selection-sort
Sorting algorithm
import java.util.Arrays;
import java.util.Scanner;

public class selection {
    public static void main(String [] args)
    {
        int i;
        Scanner in = new Scanner(System.in);
        int []arr=new int[5];
        System.out.println("Enter 5 elements in an array");
        for ( i = 0; i < arr.length; i++)
        {arr[i]=in.nextInt();}
        System.out.println("Array before sorting");
        System.out.println(Arrays.toString(arr));
        selection(arr);
        System.out.println("Array after sorting");
        System.out.println(Arrays.toString(arr));
    }
    static void selection(int []arr)
    {
        int i,j;
        for ( i = 0; i < arr.length ; i++) {
            int last = arr.length - 1 - i;
            int maxindex = getmaxindex(arr, 0, last);
            swap(arr, maxindex, last);
        }
    }
    static int getmaxindex(int []arr,int start,int last)
    {
        int max=start;
        for (int i = start; i <= last; i++) {
            if (arr[max] < arr[i]) {
                max = i;
            }
        }
            return max;
    }
    static void swap(int []arr,int first,int second)
    {
        int temp=arr[first];
        arr[first]=arr[second];
        arr[second]=temp;
    }
}
