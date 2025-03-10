# somename
# Zadacha 1

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp72
{
    internal class Program
    {
        static void Main(string[] args)
        {
            int N = int.Parse(Console.ReadLine());
            int[,] matrix = new int[N, N];

            for (int i = 0; i < N; i++)
            {
                string[] input = Console.ReadLine().Split(' ');
                for (int j = 0; j < N; j++)
                {
                    matrix[i, j] = int.Parse(input[j]);
                }
            }
            int diagonalsSum = 0;

            for (int i = 0; i < N; i++)
            {
                diagonalsSum += matrix[i, i];
            }

            Console.WriteLine(diagonalSum);
            Console.ReadLine();
        }
    }
}
