using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Exam_5
{
    class Program
    {
        static void Main(string[] args)
        {
            int n = int.Parse(Console.ReadLine());

            char dot = '.';
            char at = '@';

            Console.WriteLine("{0}", new string('*', n * 2 + 1));
            Console.WriteLine(".*{0}*.", new string(' ', (n * 2 + 1) - 4));
            for (int i = 1; i <= n - 2; i++)
            {
                Console.WriteLine("{0}*{1}*{0}", new string(dot, i + 1), new string(at, (n * 2 + 1) - 4 - (i * 2)));                
            }
            Console.WriteLine("{0}*{0}", new string('.', n));
            for (int i = 1; i <= n - 2; i++)
            {
                Console.WriteLine("{0}*{1}@{1}*{0}", new string('.', n - i), new string(' ',(i - 2) + 1));
            }
            Console.WriteLine(".*{0}*.", new string('@', (n * 2 + 1) - 4));
            Console.WriteLine("{0}", new string('*', n * 2 + 1));
        }
    }
}
