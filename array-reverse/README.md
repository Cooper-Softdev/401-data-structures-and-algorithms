# Array Reverse

Given an array of any size reverse that array as the return of a function without using any built-in methods.

## Whiteboard Process

<img width="711" alt="Screenshot 2023-07-10 at 11 27 58 PM" src="https://github.com/Cooper-Softdev/401-data-structures-and-algorithms/assets/73309872/8198ebd9-d180-430f-b458-58d486b579a1">

## Approach & Efficiency

Approach was to use the stack underflow from today's lecture to cause the index to underflow to the last one of the array, this should allow the function to work with an array of any size. Once i is on index -1 of the given array that can be added to the new reversed array as index 0 and iterated from there both ways until reaching the end and beginning, respectively.

Asking GPT wtf Big O is, it said that this could be more efficient if I were to use Collections.reverse(list); then array = list.toArray(array); since this wouldn't create a new array therefore being more computationally and memory efficient. If you ever wanted to ask someone "why?" 1000 times in a row and not get murdered...

## Solution

public class Main {
    public static void main(String[] args) {
        int[] arr = {1, 2, 3, 4, 5, 6};
        int[] reversedArr = reverseArray(arr);

        // Print the reversed array
        for (int i : reversedArr) {
            System.out.print(i + " ");
        }
    }

    public static int[] reverseArray(int[] arr) {
        int[] reversedArr = new int[arr.length];
        for (int i = 0; i < arr.length; i++) {
            reversedArr[i] = arr[arr.length - 1 - i];
        }
        return reversedArr;
    }
}
