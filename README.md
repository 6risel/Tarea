using System;
using System.Linq;

class Ejercicio1
{
    static void Main()
    {
        Console.WriteLine("--- EJERCICIO 1 ---");
        double[] notas = new double[6];

        for (int i = 0; i < 6; i++)
        {
            Console.Write($"Ingrese la nota {i + 1}: ");
            notas[i] = double.Parse(Console.ReadLine());
        }

        double menorNota = notas.Min();
        double suma = notas.Sum() - menorNota;
        double promedio = suma / 5.0;

        Console.WriteLine($"\nNota eliminada: {menorNota}");
        Console.WriteLine($"El promedio final es: {promedio:F2}");
    }
}
