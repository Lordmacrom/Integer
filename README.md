# Integer

﻿using System;

public class Program
{
    public static void Main(string[] args)
    {
        int i, j, n;
        int[] tab2;


        Console.WriteLine("Podaj wartości całkowite oddzielone przecinkami:");

        string[] tab = Console.ReadLine().Split(',');

        tab2 = new int[tab.Length];

        for (i = 0; i < tab.Length; i++)
        {
            tab2[i] = Convert.ToInt32(tab[i]);
        }

        for (i = 0; i < tab2.Length; i++)
        {
            n = 0;
            for (j = 0; j < tab2.Length; j++)
            {
                if (tab2[i] == tab2[j])
                    n++;
            }
            if (n % 2 != 0)
            {
                Console.WriteLine("Wynik to: \n{0}", tab2[i]);
                Environment.Exit(0);
            }
        }


    }
}
