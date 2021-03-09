# Lab2
package com.xsis.example;


import java.util.Scanner;
import java.util.Random;
import java.text.DecimalFormat;

public class Main
{

    public static void main(String[] args)
    {

        Random random = new Random();
        int input, input1, input2;
        int digit1 = random.nextInt(9-0);
        int digit2 = random.nextInt(9-0);


            System.out.println("Nomor Lotre Hari Ini: " + digit1 + "" + digit2);
        do
        {
            Scanner baca =  new Scanner(System.in);
                System.out.println("Masukan nomor lotre anda [0-99]: ");
                input = baca.nextInt();
        }
        while (input >= 99 && input <= 0);


        DecimalFormat For = new DecimalFormat("00");
            String inputFor = For.format(input);
            
            //cari dari char ke int
            input1 = Character.getNumericValue(inputFor.charAt(0));
            input2 = Character.getNumericValue(inputFor.charAt(1));

            if (input1 == digit1 && input2 == digit2) {
                System.out.println("Anda menang dan mendapatkan uang senilai $10000");
            } else if (input1 == digit2 && input2 == digit1) {
                System.out.println("Anda menang dan mendapatkan uang senilai $3000");
            } else if (input1 == digit1 || input2 == digit2 || input1 == digit2 || input2 == digit1) {
                System.out.println("Anda menang dan mendapatkan uang senilai $1000");
            } else {
                System.out.println("Anda kalah");
            }
    }
}
