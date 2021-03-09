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
        int random_digit1 = random.nextInt(9-0);
        int random_digit2 = random.nextInt(9-0);
        int input, input1, input2;

            System.out.println("Nomor Lotre Hari Ini: " + random_digit1 + "" + random_digit2);

        Scanner baca =  new Scanner(System.in);
            System.out.println("Masukan nomor lotre anda : ");
            input = baca.nextInt();

        DecimalFormat For = new DecimalFormat("00");

        if (input >= 99 )
        {
            System.out.println("Tidak diproses");
        }
        else {
            String inputFor = For.format(input);

            input1 = Character.getNumericValue(inputFor.charAt(0));
            input2 = Character.getNumericValue(inputFor.charAt(1));

            if (input1 == random_digit1 && input2 == random_digit2) {
                System.out.println("Anda menang dan mendapatkan uang senilai $10000");
            } else if (input1 == random_digit2 && input2 == random_digit1) {
                System.out.println("Anda menang dan mendapatkan uang senilai $3000");
            } else if (input1 == random_digit1 || input2 == random_digit2 || input1 == random_digit2 || input2 == random_digit1) {
                System.out.println("Anda menang dan mendapatkan uang senilai $1000");
            } else {
                System.out.println("Anda kalah");
            }
        }
    }
}
