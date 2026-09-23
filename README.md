using System;

class Program
{
    static void Main()
    {
        double[] notas = new double[6];
        double suma = 0;
        double menor;

        for (int i = 0; i < 6; i++)
        {
            Console.Write("Ingrese la nota " + (i + 1) + ": ");
            notas[i] = double.Parse(Console.ReadLine());
            suma += notas[i];
        }

        menor = notas[0];

        for (int i = 1; i < 6; i++)
        {
            if (notas[i] < menor)
            {
                menor = notas[i];
            }
        }

        suma -= menor;

        double promedio = suma / 5;

        Console.WriteLine("La menor nota eliminada es: " + menor);
        Console.WriteLine("El promedio es: " + promedio);
    }
}
