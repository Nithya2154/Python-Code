# Students Mark Analysis

This project analyzes the marks of 20 students across 5 subjects using Python and NumPy.

## Features

- **Randomly generated marks** for each student in each subject
- Compute **averages** by subject and student
- Find **highest and lowest marks** per subject
- Identify the **overall topper** by average and total marks
- **Pass count** per subject (marks ≥ 40 are considered passing)
- Determine the **most difficult subject** (lowest average)
- **Rank students** based on total marks

## How It Works

- The script generates a NumPy array of marks (integers between 10 and 100)
- Analytical outputs are printed for:
    - Subject-wise and student-wise averages
    - Highest and lowest marks in every subject
    - The student(s) with the highest average and highest total marks
    - Pass count per subject (marks ≥ 40)
    - The subject considered most difficult (lowest average)
    - Student ranking based on total marks

## Requirements

- Python 3
- NumPy library

## How to Run

1. Make sure you have Python and NumPy installed:
    ```bash
    pip install numpy
    ```
2. Run the script:
    ```bash
    python Students_mark_analysis.py
    ```
3. Observe the results in your console.

## Example Output

```
Average by Subjects: [66.8 63.75 53.3 61.5 56.85]
Average by Students: [69.8 61.0 54.0 ...]
Highest Marks of Subject: [97 99 93 98 94]
Lowest Marks of Subject: [18 11 10 18 13]
Topper of the Class: 0 with Average of 69.8
Pass Count By Subject: [18 17 14 17 15]
The Difficult Subject Is: 2
Ranking: [ 1  5 12  7 ...]
```

## License

This project is open-sourced under the MIT License.
