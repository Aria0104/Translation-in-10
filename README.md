```C#
Console.WriteLine("Введите число");
double number = Convert.ToDouble(Console.ReadLine());
Console.WriteLine("Введите систему счисления (от 2 до 9)");
int number_system = Convert.ToInt32(Console.ReadLine());

while (true)
{
    if (number_system >= 2 && number_system <= 9)
    { break; }

    else
    {
        Console.WriteLine("шаг не должен равнять нулю. попробуйте еще раз");
        number_system = Convert.ToInt32(Console.ReadLine());
    }
}
;

double balalala = 0;
double total_answer = 0;

string count = number.ToString();
int stepen_plus = 0;

for (int i = 0; i < count.Length; i++)
{
    balalala = Math.Floor(number / Math.Pow(10, i)) % 10;
    total_answer += balalala * Math.Pow(number_system, stepen_plus);
    stepen_plus++;
}
Console.WriteLine($"Результат: {total_answer}");
```
