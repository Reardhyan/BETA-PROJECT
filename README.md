# BETA-PROJECT

import java.util.Scanner;

public class ArraySatuDimensi {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        int[] arr = new int[5];
        System.out.println("Masukkan 5 angka:");
        for (int i = 0; i < arr.length; i++) {
            arr[i] = input.nextInt();
        }
        System.out.println("Angka yang dimasukkan:");
        for (int i = 0; i < arr.length; i++) {
            System.out.print(arr[i] + " ");
        }
    }
}
