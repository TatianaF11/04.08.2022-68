void Zadacha68()
{
//Задача 68: Напишите программу вычисления функции Аккермана с помощью рекурсии.
//Даны два неотрицательных числа m и n.
// m = 3, n = 2 -> A(m,n) = 29
    Console.WriteLine("Введите число- М:");
    int M = Convert.ToInt32(Console.ReadLine());
    Console.WriteLine("Введите число- N:");
    int N = Convert.ToInt32(Console.ReadLine());
    Console.WriteLine(AkkermanFunction(M,N));
}

int AkkermanFunction(int m, int n)
{
    if(m == 0)
    {
        return n+1;
    }
    else if(n==0)
    {
        return AkkermanFunction(m-1,1);
    }
    else 
    {
        return AkkermanFunction(m-1,AkkermanFunction(m,n-1));
    }
}
Zadacha68();
