### Experiment-20: -

---

# Sorting Algorithms in C++

This repository contains implementations of various sorting algorithms written in C++. Each algorithm is implemented in its own code block to illustrate the functionality of basic sorting techniques, including Selection Sort, Insertion Sort, and Bubble Sort.

## Overview

The repository contains C++ code for:

1. **Selection Sort**
2. **Insertion Sort**
3. **Bubble Sort**

Each program reads an array of integers from the user, applies the sorting algorithm, and outputs the sorted array.

### Files:
1. **Selection Sort:** Implements the selection sort algorithm using pointer manipulation to swap values.
2. **Insertion Sort:** Implements the insertion sort algorithm to sort an array in-place.
3. **Bubble Sort:** Uses the classic bubble sort approach to iteratively swap elements in the array.

## Compilation and Execution

### Prerequisites:
- You need to have a C++ compiler installed (e.g., `g++` or `clang`).



### Example:

```bash
g++ selection_sort.cpp -o selection_sort
./selection_sort
```

## Sample Code Snippets

### Selection Sort
```cpp
void swap(int *a, int *b) {
    int temp = *a;
    *a = *b;
    *b = temp;
}

void s_sort(int *a, int elements) {
    int n = 0;
    int *b;
    
    while (n != elements) {
        b = a + 1;
        for (int i = 0; i < (elements - 1) - n; i++) {
            if (*a > *b) {
                swap(a, b);
            }
            b++;
        }
        n++;
        a++;
    }
}
```

### Insertion Sort
```cpp
void insertionSort(int arr[], int n) {
    for (int i = 1; i < n; i++) {
        int key = arr[i];
        int j = i - 1;
        while (j >= 0 && arr[j] > key) {
            arr[j + 1] = arr[j];
            j--;
        }
        arr[j + 1] = key;
    }
}
```

### Bubble Sort
```cpp
void swap(int* a, int* b) {
    int temp = *a;
    *a = *b;
    *b = temp;
}

void bubbleSort(int arr[], int elements) {
    int n = 0;
    while (n != elements) {
        for (int i = 0; i < elements - n; i++) {
            if (arr[i] > arr[i + 1]) {
                swap(&arr[i], &arr[i + 1]);
            }
        }
        n++;
    }
}
```

