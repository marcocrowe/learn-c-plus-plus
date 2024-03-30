# Factory Production Exercise

Given the following data

|  Day  | Factory 1   | Factory 2   | Factory 3   | Factory 4   | Factory 5   |
|-------|------------:|------------:|------------:|------------:|------------:|
| Day 1 | 130         | 225         | 155         | 165         | 145         |
| Day 2 | 134         | 241         | 153         | 161         | 146         |
| Day 3 | 129         | 244         | 149         | 157         | 145         |
| Day 4 | 131         | 239         | 150         | 161         | 151         |
| Day 5 | 120         | 209         | 148         | 130         | 140         |
| Day 6 | 72          | 40          | 47          | 66          | 44          |
| Day 7 | 22          | 28          | 21          | 26          | 23          |

## Tasks

### Task  1

Write a program to track the number of items produced in five different factories over a seven-day period. Use a two-dimensional array called `production` to store the data.

### Task 2

Calculate and present the average production for each factory over the week.

### Task 3

Calculate and present the total production for each day over the week.

## Stater code

### C++

```cpp
#include <iostream>
using namespace std; 

const int NUM_FACTORIES = 5; 
const int NUM_DAYS = 7; 

void PrintProduction(int production[NUM_DAYS][NUM_FACTORIES]);

/// <summary>
/// Print the production of the factories.  THIS IS NOT IDEAL CODE.  IT IS JUST FOR DEMONSTRATION PURPOSES.
int main()
{
    int production[NUM_DAYS][NUM_FACTORIES] = {
        {130, 225, 155, 165, 145},
        {134, 241, 153, 161, 146},
        {129, 244, 149, 157, 145},
        {131, 239, 150, 161, 151},
        {120, 209, 148, 130, 140},
        {72, 40, 47, 66, 44},
        {22, 28, 21, 26, 23}
    };
    PrintProduction(production);

    // Task 2: Calculate and present the average production for each factory over the week.

    // Task 3: Calculate and present the total production for each day over the week.
}
/// <summary>
/// Print the production of the factories.  THIS IS NOT IDEAL CODE.  IT IS JUST FOR DEMONSTRATION PURPOSES.
/// You can consider improving the code
/// </summary>
/// <param name="production"></param>
void PrintProduction(int production[NUM_DAYS][NUM_FACTORIES])
{
    cout << "Day\t";

    for (int lab = 0; lab < NUM_FACTORIES; lab++)
        cout << "Lab " << lab + 1 << "\t";
    cout << endl;


    for (int day = 0; day < NUM_DAYS; day++)
    {
        cout << "Day " << day + 1 << ":\t";
        for (int lab = 0; lab < NUM_FACTORIES; lab++)
            cout << production[day][lab] << "\t";
        cout << endl;
    }
    cout << endl;
}
```

### C

```c
#include <stdio.h>

#define NUM_FACTORIES 5
#define NUM_DAYS 7

/**
 * Print the production data for each factory over seven days.
 * 
 * @param production The two-dimensional array storing the production data.
 */
void print_production(int production[NUM_DAYS][NUM_FACTORIES]);

int main() {
    int production[NUM_DAYS][NUM_FACTORIES] = {
        {130, 225, 155, 165, 145},
        {134, 241, 153, 161, 146},
        {129, 244, 149, 157, 145},
        {131, 239, 150, 161, 151},
        {120, 209, 148, 130, 140},
        {72, 40, 47, 66, 44},
        {22, 28, 21, 26, 23}
    };
    print_production(production);

    // Task 2: Calculate and present the average production for each factory over the week.

    // Task 3: Calculate and present the total production for each day over the week.

    return 0;
}

/**
 * Print the production data for each factory over seven days.
 * 
 * @param production The two-dimensional array storing the production data.
 */
void print_production(int production[NUM_DAYS][NUM_FACTORIES]) {
    printf("Day\t");

    for (int factory = 0; factory < NUM_FACTORIES; factory++)
        printf("Factory %d\t", factory + 1);
    printf("\n");

    for (int day = 0; day < NUM_DAYS; day++) {
        printf("Day %d:\t", day + 1);
        for (int factory = 0; factory < NUM_FACTORIES; factory++)
            printf("%d\t", production[day][factory]);
        printf("\n");
    }
    printf("\n");
}
```

### Python

```python
def print_production(production):
    """
    Print the production data for each factory over seven days.

    Args:
        production: A two-dimensional list storing the production data.
    """
    print("Day\t", end="")
    for factory in range(len(production[0])):
        print(f"Factory {factory + 1}\t", end="")
    print()

    for day, productions in enumerate(production, 1):
        print(f"Day {day}:\t", end="")
        for prod in productions:
            print(f"{prod}\t", end="")
        print()

def main():
    """
    The main function to execute the program.
    """
    production = [
        [130, 225, 155, 165, 145],
        [134, 241, 153, 161, 146],
        [129, 244, 149, 157, 145],
        [131, 239, 150, 161, 151],
        [120, 209, 148, 130, 140],
        [72, 40, 47, 66, 44],
        [22, 28, 21, 26, 23]
    ]
    print_production(production)

    # Task 2: Calculate and present the average production for each factory over the week.

    # Task 3: Calculate and present the total production for each day over the week.

if __name__ == "__main__":
    main()
```

### Java

```java
public class FactoryProduction {
    
    /**
     * Print the production data for each factory over seven days.
     * 
     * @param production A two-dimensional array storing the production data.
     */
    public static void printProduction(int[][] production) {
        System.out.print("Day\t");
        
        for (int factory = 0; factory < production[0].length; factory++)
            System.out.print("Factory " + (factory + 1) + "\t");
        System.out.println();
        
        for (int day = 0; day < production.length; day++) {
            System.out.print("Day " + (day + 1) + ":\t");
            for (int factory = 0; factory < production[0].length; factory++)
                System.out.print(production[day][factory] + "\t");
            System.out.println();
        }
    }
    
    /**
     * The main method to execute the program.
     * 
     * @param args The command-line arguments.
     */
    public static void main(String[] args) {
        int[][] production = {
            {130, 225, 155, 165, 145},
            {134, 241, 153, 161, 146},
            {129, 244, 149, 157, 145},
            {131, 239, 150, 161, 151},
            {120, 209, 148, 130, 140},
            {72, 40, 47, 66, 44},
            {22, 28, 21, 26, 23}
        };
        printProduction(production);

        // Task 2: Calculate and present the average production for each factory over the week.

        // Task 3: Calculate and present the total production for each day over the week.
    }
}
```

### C Sharp

```csharp
using System;

class FactoryProduction
{
    /// <summary>
    /// Print the production data for each factory over seven days.
    /// </summary>
    /// <param name="production">A two-dimensional array storing the production data.</param>
    static void PrintProduction(int[,] production)
    {
        Console.Write("Day\t");

        for (int factory = 0; factory < production.GetLength(1); factory++)
            Console.Write($"Factory {factory + 1}\t");
        Console.WriteLine();

        for (int day = 0; day < production.GetLength(0); day++)
        {
            Console.Write($"Day {day + 1}:\t");
            for (int factory = 0; factory < production.GetLength(1); factory++)
                Console.Write($"{production[day, factory]}\t");
            Console.WriteLine();
        }
    }

    /// <summary>
    /// The main method to execute the program.
    /// </summary>
    /// <param name="args">Command-line arguments.</param>
    static void Main(string[] args)
    {
        int[,] production = {
            {130, 225, 155, 165, 145},
            {134, 241, 153, 161, 146},
            {129, 244, 149, 157, 145},
            {131, 239, 150, 161, 151},
            {120, 209, 148, 130, 140},
            {72, 40, 47, 66, 44},
            {22, 28, 21, 26, 23}
        };
        PrintProduction(production);

        // Task 2: Calculate and present the average production for each factory over the week.

        // Task 3: Calculate and present the total production for each day over the week.
    }
}
```

PHP

```php
<?php

/**
 * Print the production data for each factory over seven days.
 *
 * @param array $production A two-dimensional array storing the production data.
 * @return void
 */
function printProduction($production) {
    echo "Day\t";
    
    foreach ($production[0] as $factory => $value) {
        echo "Factory " . ($factory + 1) . "\t";
    }
    echo "\n";

    foreach ($production as $day => $productions) {
        echo "Day " . ($day + 1) . ":\t";
        foreach ($productions as $prod) {
            echo $prod . "\t";
        }
        echo "\n";
    }
}

/**
 * The main function to execute the program.
 *
 * @return void
 */
function main() {
    $production = [
        [130, 225, 155, 165, 145],
        [134, 241, 153, 161, 146],
        [129, 244, 149, 157, 145],
        [131, 239, 150, 161, 151],
        [120, 209, 148, 130, 140],
        [72, 40, 47, 66, 44],
        [22, 28, 21, 26, 23]
    ];
    printProduction($production);

    // Task 2: Calculate and present the average production for each factory over the week.

    // Task 3: Calculate and present the total production for each day over the week.
}

// Execute the main function
main();
?>
```

---
