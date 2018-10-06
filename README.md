# arkademySoal
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package arkademytest;

import java.text.DateFormat;
import java.text.SimpleDateFormat;
import java.util.Date;
import java.util.concurrent.TimeUnit;

/**
 *
 * @author hadhiee
 */
public class ArkademyTest {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO code application logic here
        soal01(10);
        soal02(10);
        soal03();
        soal04(100);
        soal05("arkademy");
        soal06("abcdefghijklmnopqrastuvwxyz");

    }

    public static void soal06(String data) {
        System.out.println("SOAL NO 6\n");
        char[] huruf = new char[data.length()];
        for (int i = 0; i < data.length(); i++) {
            huruf[i] = data.charAt(i);

        }
        int t = 0;
        for (int i = 0; i < huruf.length; i++) {
            if (huruf[i] == 'm') {
                t = i + 1;
            }

        }

        System.out.println("huruf \'m\' ada diposisi = " + t);
        System.out.println("");
    }

    public static void soal05(String data) {
        System.out.println("SOAL NO 5\n");
        char[] huruf = new char[data.length()];
        for (int i = 0; i < data.length(); i++) {
            huruf[i] = data.charAt(i);

        }
        int t = 0;
        for (int i = 0; i < huruf.length; i++) {
            if (huruf[i] == 'a') {
                t = t + 1;
            }

        }

        System.out.println("huruf \'a\' ada sebanyak = " + t);
        System.out.println("");
    }

    public static void soal04(int data) {
        System.out.println("SOAL NO 4\n");
        try {
            int[] angka = new int[data];
            int k = 0;
            String[] huruf = new String[data];
            for (int i = 0; i < data; i++) {
                angka[i] = i;
                huruf[i] = Integer.toString(i);

            }
            for (int i = 0; i < huruf.length; i++) {
                int a=huruf[i].length();
                for (int j = 0; j < a; j++) {
                    if(huruf[i].charAt(j)=='3')
                    k=k+1;
                    
                }

            }
            System.out.println("angka \'3\' dalam 100 angka ada sebanyak = " + k + " kali\n");
        } catch (Exception e) {
            System.out.println("kesalahan...");
        }
    }

    public static void soal03() {
        try {
            System.out.println("SOAL NO 3\n");
            String cIn = "2018-10-05";
            SimpleDateFormat date = new SimpleDateFormat("yyyy-MM-dd");
            Date tglCin = (Date) date.parse(cIn);

            String cOut = "2018-11-01";
            Date tglCout = (Date) date.parse(cOut);
            long lama = Math.abs(tglCout.getTime() - tglCin.getTime());
            long sel = TimeUnit.MILLISECONDS.toDays(lama);
            System.out.println("selisih hari yaitu : " + sel + " hari");
        } catch (Exception e) {
            System.out.println("kesalahan..");
        }
        System.out.println("");
    }

    public static void soal02(int data) {
        int[] angka = new int[data];
        System.out.println("SOAL NO 2\n");
        int n1 = 0, n2 = 1, n3, i, count = data;
        System.out.print(n1 + " " + n2);//printing 0 and 1    

        for (i = 2; i < count; ++i)//loop starts from 2 because 0 and 1 are already printed    
        {
            n3 = n1 + n2;
            System.out.print(" " + n3);
            n1 = n2;
            n2 = n3;
        }
        System.out.println("\n");
    }

    public static void soal01(int data) {
        int[] angka = new int[data];
        System.out.println("SOAL NO 1\n");
        for (int i = 0; i < data; i++) {
            angka[i] = i + 1;

        }
        for (int i = 0; i < angka.length; i++) {
            for (int j = i; j < angka.length - 1; j++) {
                System.out.print(angka[j] + " ");

            }
            System.out.println("");
        }

    }

}
