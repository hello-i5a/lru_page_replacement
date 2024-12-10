# LRU Page Replacement Algorithm with Visualization

Implementation of the Least Recently Used (LRU) page replacement algorithm in Python.

## Features

- **LRU Page Replacement Simulation**: Simulates the behavior of the LRU algorithm when accessing a sequence of pages.
- **Dynamic Input**: Allows the user to input the number of memory frames and the page reference string.
- **Page Hit and Fault Tracking**: Keeps track of the number of page hits and faults during the simulation.
- **Interactive Visualization**: Displays a step-by-step table of page accesses, with frames and the hit/fault status for each step.
- **Metrics**: Calculates and prints the hit ratio and fault ratio after simulation.

## Code Explanation

### LRUPageReplacement Class

This class simulates the LRU page replacement algorithm. It has the following attributes and methods:

- **Attributes**:

  - `num_frames`: The number of memory frames available for storing pages.
  - `frames`: A list that stores the pages currently in memory.
  - `page_faults`: Counter for the number of page faults.
  - `page_hits`: Counter for the number of page hits.
  - `page_sequence`: The list of pages being accessed.
  - `page_steps`: A list that tracks the state of memory frames and whether each access resulted in a hit or fault.

- **Methods**:
  - `access_page(page)`: Simulates accessing a page, updating the state of memory frames, and recording hits and faults.
  - `simulate(page_sequence)`: Simulates the page access sequence.
  - `print_results()`: Prints statistics such as the total number of page hits, faults, and their ratios.
  - `display_table()`: Creates and displays an interactive Plotly table showing the memory state after each page access.

## Running the Program

1. **Dependencies**

   The project requires the following Python libraries:

   - `matplotlib`
   - `pandas`

2. **Running the Notebook**
   - Open the `main.ipynb` notebook in a Jupyter Notebook environment.
   - Run each cell sequentially to execute the program.
   - The program will prompt you for 1) the number of memory frames and 2) the page reference sequence.
   - After entering the input, the program will simulate the LRU page replacement and generate a plot that shows how the pages are loaded into memory, with the number of page faults displayed in the plot title.
