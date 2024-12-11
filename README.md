# PDC-ASSIGNMENT
# Payment Pattern Analysis

This project analyzes student fee payment patterns to determine the most frequent payment day for each student. It processes the data from two CSV files (`students.csv` and `student_fees.csv`) and outputs a merged file with student details and their most consistent payment day.

---

## Features

- **Parallel Execution**: Optimized using multiprocessing to improve performance on large datasets.
- **Serial Execution**: A simpler, sequential approach for comparison.
- **Data Handling**: Handles missing values and ensures data integrity.
- **CSV Output**: Saves the results into separate output files for parallel and serial processing.

---

## Project Files

- `students.csv`: Contains student details such as `Student ID`, `Name`, and `Age`.
- `student_fees.csv`: Contains fee payment records with `Student ID` and `Payment Date`.
- `parallel_processing.py`: Implements the parallel execution of payment pattern analysis.
- `serial_processing.py`: Implements the serial execution of payment pattern analysis.
- `README.md`: Documentation for the project.

---

## Requirements

### Dependencies

- Python 3.x
- Pandas

Install the required Python libraries using:
```bash
pip install pandas
```

### System Requirements

- For **parallel processing**, ensure your system supports multiprocessing with multiple cores.

---

## Usage

### 1. Parallel Processing
Run the `parallel_processing.py` file:
```bash
python parallel_processing.py
```
**Output**: Merged data will be saved to `parallel_output.csv`.

### 2. Serial Processing
Run the `serial_processing.py` file:
```bash
python serial_processing.py
```
**Output**: Merged data will be saved to `serial_output.csv`.

---

## Example Input/Output

### Input Files

#### `students.csv`
| Student ID | Name         | Age |
|------------|--------------|-----|
| 101        | John Smith   | 21  |
| 102        | Alice Brown  | 22  |
| 103        | Bob Johnson  | 20  |

#### `student_fees.csv`
| Student ID | Payment Date |
|------------|--------------|
| 101        | 2023-10-15   |
| 102        | 2023-10-10   |
| 101        | 2023-11-15   |
| 103        | 2023-10-20   |

### Output File (`*_output.csv`)
| Student ID | Name         | Age | Most Consistent Payment Day |
|------------|--------------|-----|-----------------------------|
| 101        | John Smith   | 21  | 15                          |
| 102        | Alice Brown  | 22  | 10                          |
| 103        | Bob Johnson  | 20  | 20                          |

---

## Performance

### Parallel Execution
- **Pros**: Faster on large datasets, especially with multiple CPU cores.
- **Cons**: Slightly more complex codebase.

### Serial Execution
- **Pros**: Simpler implementation.
- **Cons**: Slower execution, especially on large datasets.

---

## Execution Time

Linear Execution
Start Time: 2024-12-10 19:42:38.056700

End Time: 2024-12-10 19:42:56.945347

Total Time: 20.88 seconds

Parallel Execution
Start Time: 2024-12-10 19:47:44.715000

End Time: 2024-12-10 19:47:48.288306

Total Time: 04.57 seconds



