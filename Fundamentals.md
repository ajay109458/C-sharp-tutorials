
# Fundamentals

### Variables
```
using System;

namespace ConsoleApp1
{
    class Program
    {
        static void Main(string[] args)
        {
            int myAge = 21;
            int x = 5;
            double myHourlyRate = 150.00;
            var myName = "Ajay Yadav";  //Hey compiler identify the type of this variable. 
            Console.WriteLine($"myAge: {myAge}, x: {x}, myHourlyRate: {myHourlyRate}, MyName: {myName}");
        }
    }
}

```

### If Statement
```
using System;

namespace ConsoleApp1
{
    class Program
    {
        static void Main(string[] args)
        {
            int a = 20;
            int b = 26;
            int c = 54;
            int d = 60;

            if (a > 18)
            {
                Console.WriteLine("A can vote");
            }

            if (a >= 21 && b >= 21)
            {
                Console.WriteLine("A and B both can drink");
            }
            else if (a >= 21 || b >= 21)
            {
                Console.WriteLine("At least one can drink");
            }
        }
    }
}
```

### For Loop 
```
using System;

namespace ConsoleApp1
{
    class Program
    {
        static void Main(string[] args)
        {
            for (int i = 0; i < 300; i++)
            {
                Console.WriteLine($"Hello {i.ToString()}");
            }
        }
    }
}
```

### While Loop
```
using System;

namespace ConsoleApp1
{
    class Program
    {
        static void Main(string[] args)
        {
            int myLittleHorses = 0;
            while (myLittleHorses < 10)
            {
                Console.WriteLine($"My Little horses: {myLittleHorses}");
                myLittleHorses++;
            }
        }
    }
}
```

### Constants 
Constants are assigned a value that never changes. 

### Enumerated Constants
* Give an individual value to each of a set. 
* Can greatly simplify programming. 
* Unless you tell it differently, starts at zero and increment by 1. 

```
enum Actions
{
  Create,
  Update,
  Delete
}
```

```
using System;

namespace ConsoleApp1
{
    class Program
    {
        enum Ages
        {
            OldEnough = 5,
            CanDrink = 21,
            TooOld = 90
        }

        static void Main(string[] args)
        {
            const int age = 20;

            if (age < (int)Ages.CanDrink)
            {
                Console.WriteLine("You are not allowed to drink.");
            }
        }
    }
}
```

### Switch 
```
namespace ConsoleApp1
{
    class Program
    {
        enum Movies
        {
            Don,
            Superman,
            Batman
        }

        static void Main(string[] args)
        {
            Movies bestMovie = Movies.Superman;

            switch (bestMovie)
            {
                case Movies.Batman:
                    Console.WriteLine("Batman is best Movie");
                    break;
                case Movies.Superman:
                    Console.WriteLine("Superman is best Movie");
                    break;
                case Movies.Don:
                    Console.WriteLine("Don is best Movie");
                    break;
                default:
                    Console.WriteLine("You need to make a choice");
                    break;
            }
        }
    }
}
```
