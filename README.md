# README for Backpack Project: Artifact Value Optimization

## Overview

`backpack.c` is a C program that tackles a classic optimization problem often referred to as the "Knapsack Problem". This program reads data from a file to build a list of artifacts, each with specific weight and value attributes. It then calculates the maximum possible value of artifacts that can be carried in a backpack with a given weight limit. The solution is implemented using both a brute-force approach and an optimized approach with memoization.

## Features

- **Data Reading**: Reads artifact data from a file.
- **Brute-Force Algorithm**: Computes the maximum value using a basic recursive approach.
- **Optimized Algorithm**: Computes the maximum value using a memoized recursive approach for better performance.
- **Dynamic Memory Management**: Allocates and deallocates memory dynamically for efficient use.

## File Structure

### Source File

- **`backpack.c`**: Contains the main logic of the program, including:
  - Data structures
  - Function implementations
  - Main program execution flow

### Data File

- **`collection1.txt`**, **`collection2.txt`**, **`collection3.txt`**, **`collection4.txt`**: Sample data files containing artifact details.

## Compilation

To compile the `backpack.c` source file, use the following command:

```bash
gcc -o backpack backpack.c
```

This command will generate an executable named `backpack`.

## Usage

1. **Run the Program**

   Execute the compiled program:

   ```bash
   ./backpack
   ```

2. **Input Prompts**

   - **Collection Number**: Enter the collection number (1, 2, 3, or 4) corresponding to the data file to read.
   - **Weight Limit**: Enter the maximum weight capacity of the backpack.

3. **Output**

   - **List of Artifacts**: Displays the artifacts with their weight and value.
   - **Total Weight and Value**: Shows the total weight and value of all artifacts.
   - **Maximum Value (Slow Mode)**: Displays the maximum value using the brute-force approach (for collections 1, 2, and 3).
   - **Maximum Value (Fast Mode)**: Displays the maximum value using the optimized approach with memoization.
   - **Artifacts to Put in Backpack**: Displays the list of artifacts that maximize value while staying under the weight limit (this part is a placeholder and needs additional implementation for extra credit).

## Functions

- **`totalWeight`**: Calculates the total weight of a list of artifacts.
- **`totalValue`**: Calculates the total value of a list of artifacts.
- **`maxValueFromHere`**: Computes the maximum value from the current artifact index using a brute-force approach.
- **`maxValueFromStart`**: Initializes the computation of the maximum value from the start using the brute-force approach.
- **`maxValueFromHereFast`**: Computes the maximum value using a memoized recursive approach.
- **`maxValueFromStartFast`**: Initializes the computation of the maximum value from the start using the memoized approach.
- **`readCollectionFile`**: Reads artifact data from a specified file and constructs the artifact array.
- **`printArtifacts`**: Prints out the details of each artifact.

## Memory Management

The program dynamically allocates memory for the artifact array and memoization table. It is crucial to free this memory after use to avoid memory leaks.

## Known Issues

- The part of the code to print the artifacts to put in the backpack to maximize value is incomplete and marked with a TODO comment. This feature can be extended for extra credit.

## License

This program is provided for educational purposes under the terms of the license for the course.

---

Feel free to adjust any details as necessary for your specific needs or guidelines!
