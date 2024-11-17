# LRU Page Replacement Algorithm with Visualization

Implementation of the Least Recently Used (LRU) page replacement algorithm in Python.

## Features

- **Simulates LRU Page Replacement**: The program simulates the Least Recently Used (LRU) page replacement algorithm to manage memory frames and handle page faults.
- **User Input**: Prompts the user to input the number of frames (memory slots) and a sequence of page accesses (space-separated).
- **Visualization**: Uses **matplotlib** to plot the page replacement process, showing the pages present in the frames at each time step.
- **Page Fault Counting**: The program tracks and displays the total number of page faults during the simulation.

## Explanation of the Code

The program simulates the LRU page replacement algorithm, which replaces the least recently used page when a page needs to be loaded but no free space is available in memory.

### Key Functions

1. **`lru_page_replacement(frames_count, page_sequence)`**:

   - This function simulates the LRU algorithm by iterating through the sequence of page accesses.
   - If a page is accessed that is **not in memory**, it is added to the frame, and a page fault is recorded. If the memory is full, the **least recently used** page (the one that was accessed the least recently) is removed.
   - If the page is already in memory, it is moved to the most recently used position.
   - It returns the total number of page faults and the history of the frames' states (to be used for plotting).

2. **`visualize_lru(frames_count, page_sequence)`**:

   - This function visualizes the LRU algorithm's behavior. It calls `lru_page_replacement` to simulate the page replacements and uses **matplotlib** to plot the frames over time.
   - The plot shows the state of the memory at each time step, where the x-axis represents time (page accesses), and the y-axis shows the pages loaded in memory frames.

3. **`main()`**:
   - The main function that handles user input for the number of frames and page reference sequence.
   - It then calls `visualize_lru` to display the simulation and generate the plot.

### LRU Algorithm Workflow

- When a page access occurs:

  1. **Page Hit**: If the page is already in memory, it is moved to the most recently used position.
  2. **Page Fault**: If the page is not in memory, it is added. If the memory is full, the **least recently used page** is evicted and replaced by the new page.

  The algorithm continues this process for all page accesses in the given sequence.

## Running the Program

1. **Dependencies**

   The project requires the following Python libraries:

   - `matplotlib`

2. **Running the Notebook**
   - Open the `main.ipynb` notebook in a Jupyter Notebook environment.
   - Run each cell sequentially to execute the program.
   - The program will prompt you for 1) the number of memory frames and 2) the page reference sequence.
   - After entering the input, the program will simulate the LRU page replacement and generate a plot that shows how the pages are loaded into memory, with the number of page faults displayed in the plot title.
