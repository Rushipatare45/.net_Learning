using System;
using System.Globalization;

class Program
{
    static void Main()
    {
        Console.Write("Enter a value: ");
        string userInput = Console.ReadLine();

        // Integer Conversion
        if (int.TryParse(userInput, out int intValue))
            Console.WriteLine($"Integer: {intValue} (Valid)");
        else
            Console.WriteLine("Integer: Invalid");

        // Float Conversion
        if (float.TryParse(userInput, out float floatValue))
            Console.WriteLine($"Float: {floatValue} (Valid)");
        else
            Console.WriteLine("Float: Invalid");

        // Double Conversion
        if (double.TryParse(userInput, out double doubleValue))
            Console.WriteLine($"Double: {doubleValue} (Valid)");
        else
            Console.WriteLine("Double: Invalid");

        // Decimal Conversion
        if (decimal.TryParse(userInput, out decimal decimalValue))
            Console.WriteLine($"Decimal: {decimalValue} (Valid)");
        else
            Console.WriteLine("Decimal: Invalid");

        // Boolean Conversion
        if (bool.TryParse(userInput, out bool boolValue))
            Console.WriteLine($"Boolean: {boolValue} (Valid)");
        else
            Console.WriteLine("Boolean: Invalid");

        // DateTime Conversion
        if (DateTime.TryParseExact(userInput, "yyyy-MM-dd", CultureInfo.InvariantCulture, DateTimeStyles.None, out DateTime dateValue))
            Console.WriteLine($"DateTime: {dateValue} (Valid)");
        else
            Console.WriteLine("DateTime: Invalid");
    }
}