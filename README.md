# bubblesort_using_java
#the code goes as:
<br>
import java.util.Scanner;
<br>
public class BubbleSort
{
    public static void main(String args[]) 
    <br>
    {
        Scanner in = new Scanner(System.in);
        int arr[] = new int[20];
        System.out.println("Enter 20 numbers:");

        for (int i = 0; i < arr.length; i++) {
            arr[i] = in.nextInt();
        }

        //Sort first half in ascending order
        for (int i = 0; i < 9; i++) {
            for (int j = 0; j < (9-i); j++) {
                if (arr[j] > arr[j + 1]) {
                    int t = arr[j + 1];
                    arr[j + 1] = arr[j];
                    arr[j] = t;
                }
            }  
        }

        //Sort second half in descending order
        for (int i = 0; i < 9; i++) {
            for (int j = 10; j < (19-i); j++) {
                if (arr[j] < arr[j + 1]) {
                    int t = arr[j + 1];
                    arr[j + 1] = arr[j];
                    arr[j] = t;
                }
            }  
        }

        //Print the final sorted array
        System.out.println("\nSorted Array:");
        for (int i = 0; i < arr.length; i++) {
            System.out.print(arr[i] + " ");
        }
    }
}
