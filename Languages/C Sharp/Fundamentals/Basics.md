
## Basic boilerplate for C\#
```c#
namespace lab;

class Program
{
    static void Main(string[] args)
    {
        Console.WriteLine("Hello, World!");

        Console.ReadKey(); // pause so that the terminal don't close
    }
}

```

## changing the title in the top of the console
```c#
Console.Title = "Csharp Program"; 
```

## changing the font color in the console
```c#
Console.ForegroundColor = ConsoleColor.green;
```

## changing the window height of the terminal
```c#
Console.WindowHeight = 40;
```

## printing in the console
```c#
Console.WriteLine("hello meow");
```

```c#
Console.Write("hello meow");
```

## user input in the console
```c#
Console.Readline(); // the input is not saved
```

## `Console.Write()` VS `console.WriteLine()`
```c#
Console.WriteLine("What is your name? ");
Console.ReadLine();
```
```console
What is your name? 
<your answer here>
```

```c#
Console.Write("What is your name? ");
Console.ReadLine();
```
```console
What is your name? <your answer here>
```

## Beep
```c#
Console.Beep();
```

## Comment
```c#
// single line comment

/*
multi-line comment
multi-line comment
multi-line comment
*/
```



