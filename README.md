# CS_CreacionDeAplicacionesE2

****Adición de un paquete NuGet mediante la herramienta de .NET Core****

1. Abra **Program.cs**
. Debería ser parecido a este:

```csharp
Console.WriteLine("Hello, World!");
```

1. Ejecute el siguiente comando para instalar la biblioteca de Humanizer:

```bash
dotnet add package Humanizer --version 2.7.9
```

1. Agregue el siguiente contenido en la parte superior del archivo Program.cs para inicializar Humanizer:

```csharp
using Humanizer;
```

1. El archivo **Program.cs**
 ahora debería ser similar al siguiente:

```csharp
static void HumanizeQuantities()
{
    Console.WriteLine("case".ToQuantity(0));
    Console.WriteLine("case".ToQuantity(1));
    Console.WriteLine("case".ToQuantity(5));
}

static void HumanizeDates()
{
    Console.WriteLine(DateTime.UtcNow.AddHours(-24).Humanize());
    Console.WriteLine(DateTime.UtcNow.AddHours(-2).Humanize());
    Console.WriteLine(TimeSpan.FromDays(1).Humanize());
    Console.WriteLine(TimeSpan.FromDays(16).Humanize());
}
```

1. Agregue el contenido siguiente al archivo Program.cs en la parte inferior del archivo, debajo de `Console.WriteLine("Hello, World!");`
:

```csharp
Console.WriteLine("Quantities:");
HumanizeQuantities();

Console.WriteLine("\nDate/Time Manipulation:");
HumanizeDates();
```

1. Guarde el archivo (**Archivo**
>**Guardar**
 o CTRL + S
). Escriba el siguiente comando en el terminal para ejecutar la aplicación:

```bash
dotnet run
```

[![Install-Humanizer.png](https://i.postimg.cc/RZ1NwrWm/Install-Humanizer.png)](https://postimg.cc/qNRJd5cD)
