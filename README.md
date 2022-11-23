/*Напишите программу, которая принимает на вход пятизначное число и проверяет, является ли оно палиндромом.

Console.Clear();
 
void CheckPalindromicNumber(int number)
{
    if(number >= 10000)
    {
        int division1 = number / 10000;
        int remainder1 = number % 10;
 
            if(division1 == remainder1)
            {
                number = number / 10;
                int division2 = number / 100;
                int remainder2 = number % 10;
                if(division2 == remainder2)
                    Console.WriteLine("Да");
            }
            else 
            Console.WriteLine("Нет");
            
    }
    else
    Console.WriteLine("Некорректное число!");
}
 
Console.WriteLine("Введите пятизначное число:");
int number = int.Parse(Console.ReadLine()!);
CheckPalindromicNumber(number);*/



/*Hапишите программу, которая принимает на вход координаты двух точек и находит расстояние между ними в 3D пространстве.

class Point:
    def __init__(self, x, y, z):
        self.x1 = x
        self.y1 = y
        self.z1 = z
 
    def method(self, other):
        return sqrt((other.x1 - self.x1) ** 2 + (other.y1 - self.y1) ** 2 + (other.z1 - self.z1) ** 2)
 
p1 = [1, 2, 3]
p2 = [3, 2, 1]
point1 = Point(*p1)
point2 = Point(*p2)
print(point1.method(point2)) # 2.8284271247461903*/


//Напишите программу, которая принимает на вход число (N) и выдаёт таблицу кубов чисел от 1 до N.

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
 
 
class Program
{
    static int Sqr(int val)
    {
        int result = 0;
        for (int i = 1; i <= 2 * val - 1; i = i + 2)
            result += i;
        return result;
    }
    static void Main(string[] args)
    {
        int val = 9;
        for (int i = 1; i <= val; i++)
            Console.WriteLine(i + ": " + Sqr(i));
        Console.ReadKey(true);
    }
}
