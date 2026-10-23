# Sorting & Search Algorithms

> A Java implementation and performance comparison of classic sorting algorithms (Bubble Sort, Quick Sort) and Binary Search, with automated benchmarking across different array sizes.

## Features

- **Bubble Sort** — O(n²) comparison-based sort
- **Quick Sort** — O(n log n) divide-and-conquer sort with recursive partitioning
- **Binary Search** — O(log n) search on sorted arrays
- **Interactive menu** — Print, sort, search or create custom arrays at runtime
- **Benchmarking** — Compare execution times in nanoseconds across 3 input sizes

## Tech Stack

- **Language:** Java
- **Paradigm:** OOP + Recursion
- **I/O:** Java Scanner (console)

### Menu

```
1. Print array
2. Quick sort
3. Bubble sort
4. Search element after sort
5. Run Experiment
6. Create Sorted Array
0. Exit
```

## Project Structure

```
src/
├── Main.java          # Entry point + interactive menu
├── Sorter.java        # BubbleSort, QuickSort, array generation
├── Searcher.java      # Binary Search
└── Experiment.java    # Benchmarking across array sizes
```

## Algorithm Details

### Bubble Sort
- **Complexity:** O(n²) time, O(1) space
- Compare adjacent elements and swap if out of order, repeat n times

### Quick Sort
- **Complexity:** O(n log n) avg, O(n²) worst case (sorted input)
- Choose last element as pivot, partition into left (< pivot) / right (> pivot), recurse

### Binary Search
- **Complexity:** O(log n)
- Requires sorted array — repeatedly halves the search range

## Analysis

**Which sort is faster?**
Quick Sort — O(n log n) vs O(n²). At size 5000 the difference is ~50×.

**Does sorted input affect performance?**
Yes for Quick Sort — sorted array triggers worst-case O(n²) when using last element as pivot.

**Why does Binary Search need a sorted array?**
It relies on the guarantee that everything left of mid is smaller and everything right is larger.

## Key Learnings

- Algorithm choice has massive real-world impact on performance
- Quick Sort worst case = sorted input (use randomized pivot to avoid)
- JVM warmup and CPU cache can affect nanosecond measurements
- Recursion needs careful base case design to avoid stack overflow

## Author

**Yermakov Ilya**
