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

# Zadacha 2

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp27
{
    internal class Program
    {
        static void Main(string[] args)
        {
            int n = int.Parse(Console.ReadLine());
            int sum1 = 0;
            int sum2 = 0;
            int[,] intmatrix = new int[n, n];
            for (int row = 0; row < intmatrix.GetLength(0); row++)
            {
                int[] colElements = Console.ReadLine().Split(' ').Select(int.Parse).ToArray();

                for (int col = 0; col < intmatrix.GetLength(1); col++)
                {
                    intmatrix[row, col] = colElements[col];
                    if (row == col)
                    {
                        sum1 += intmatrix[row, col];
                    }
                    if(col + row == n - 1)
                    {
                        sum2 += intmatrix[row, col];
                    }
                }
            }
            int dif = Math.Abs(sum1 - sum2);
            Console.WriteLine(dif);


        }
    }
    
}

# Zadacha 3

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp27
{
    internal class Program
    {
        static void Main(string[] args)
        {
            int[] sizes = Console.ReadLine().Split(", ").Select(int.Parse).ToArray();
            int sum = 0;
            int[,] intmatrix = new int[sizes[0], sizes[1]];
            for (int row = 0; row < intmatrix.GetLength(0); row++)
            {
                int[] colElements = Console.ReadLine().Split(", ").Select(int.Parse).ToArray();

                for (int col = 0; col < intmatrix.GetLength(1); col++)
                {
                    intmatrix[row, col] = colElements[col];
                    sum += intmatrix[row, col];
                }
            }
            Console.WriteLine(intmatrix.GetLength(0));
            Console.WriteLine(intmatrix.GetLength(1));
            Console.WriteLine(sum);

        }
    }
    
}
