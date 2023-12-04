# c-

1. Fibonacci Series:
Without Recursion:
csharp
Copy code
using System;

class FibonacciWithoutRecursion
{
    static void Main()
    {
        Console.Write("Enter the number of terms: ");
        int n = int.Parse(Console.ReadLine());

        int first = 0, second = 1, next;

        Console.WriteLine("Fibonacci Series:");

        for (int i = 0; i < n; i++)
        {
            Console.Write(first + " ");

            next = first + second;
            first = second;
            second = next;
        }
    }
}
With Recursion:
csharp
Copy code
using System;

class FibonacciWithRecursion
{
    static int Fibonacci(int n)
    {
        if (n <= 1)
            return n;

        return Fibonacci(n - 1) + Fibonacci(n - 2);
    }

    static void Main()
    {
        Console.Write("Enter the number of terms: ");
        int n = int.Parse(Console.ReadLine());

        Console.WriteLine("Fibonacci Series:");

        for (int i = 0; i < n; i++)
        {
            Console.Write(Fibonacci(i) + " ");
        }
    }
}
2. Check Prime Number:
csharp
Copy code
using System;

class PrimeNumberCheck
{
    static void Main()
    {
        Console.Write("Enter a number: ");
        int num = int.Parse(Console.ReadLine());

        bool isPrime = true;

        for (int i = 2; i <= Math.Sqrt(num); i++)
        {
            if (num % i == 0)
            {
                isPrime = false;
                break;
            }
        }

        if (isPrime && num > 1)
            Console.WriteLine(num + " is a prime number.");
        else
            Console.WriteLine(num + " is not a prime number.");
    }
}
3. Check Palindrome Number:
csharp
Copy code
using System;

class PalindromeNumberCheck
{
    static void Main()
    {
        Console.Write("Enter a number: ");
        int num = int.Parse(Console.ReadLine());

        int originalNum = num;
        int reverse = 0;

        while (num > 0)
        {
            int remainder = num % 10;
            reverse = reverse * 10 + remainder;
            num /= 10;
        }

        if (originalNum == reverse)
            Console.WriteLine(originalNum + " is a palindrome number.");
        else
            Console.WriteLine(originalNum + " is not a palindrome number.");
    }
}
4. Print Factorial of a Number:
csharp
Copy code
using System;

class Factorial
{
    static void Main()
    {
        Console.Write("Enter a number: ");
        int num = int.Parse(Console.ReadLine());

        long factorial = 1;

        for (int i = 1; i <= num; i++)
        {
            factorial *= i;
        }

        Console.WriteLine("Factorial of " + num + " is: " + factorial);
    }
}
5. Check Armstrong Number:
csharp
Copy code
using System;

class ArmstrongNumberCheck
{
    static void Main()
    {
        Console.Write("Enter a number: ");
        int num = int.Parse(Console.ReadLine());

        int originalNum = num;
        int result = 0;
        int power = num.ToString().Length;

        while (num > 0)
        {
            int digit = num % 10;
            result += (int)Math.Pow(digit, power);
            num /= 10;
        }

        if (originalNum == result)
            Console.WriteLine(originalNum + " is an Armstrong number.");
        else
            Console.WriteLine(originalNum + " is not an Armstrong number.");
    }
}
6. Print Sum of Digits:
csharp
Copy code
using System;

class SumOfDigits
{
    static void Main()
    {
        Console.Write("Enter a number: ");
        int num = int.Parse(Console.ReadLine());

        int sum = 0;

        while (num > 0)
        {
            int digit = num % 10;
            sum += digit;
            num /= 10;
        }

        Console.WriteLine("Sum of digits is: " + sum);
    }
}
