# FinalProject
Developeder: Hamed Cheraghi

# Final Project Report - Student Management System

### 1. Class Structure Description
The project is built using Object-Oriented Programming (OOP) concepts:
* **Person (Base Class):** This is the main base class that has basic details like name and gender.
* **Student (Derived Class):** This class inherits from Person. It adds some more details like student_id and grades dictionary. It also uses encapsulation with @property to check inputs.
* **Course:** A separate class to keep the name and units of each course.
* **EducationalSystem:** The main manager class. It handles lists of students and courses, adds them, and runs the sorting or analysis methods.
* **Header:** A simple helper class with static methods just to print clean titles and separator lines.

### 2. Sorting Algorithms Used
The system can sort the students list in different ways using these algorithms:
* **Selection Sort:** Used in `sort_by_name` to sort the students alphabetically. It looks for the smallest name and puts it at the beginning.
* **Bubble Sort:** Used in `sort_by_id`, `sort_by_grade`, and `sort_by_unit`. It compares adjacent items in the list and swaps them if they are out of order.

### 3. Time Complexity Analysis
* **Time Complexity:** Both Selection Sort and Bubble Sort use nested loops (a loop inside another loop). Because of this, the time complexity is $O(N^2)$ for both algorithms. This is okay for a small class size, but it can get slow if we have thousands of students.
* **Space Complexity:** The sorting methods use `.copy()` to make a duplicate of the students list before sorting. This keeps the original list safe, but it takes a little bit of extra memory space.

### 4. Statistical Analysis Performed
Instead of writing normal python loops to do math, the project uses the **NumPy** library to analyze the grades data. We collect all student grades into a numpy array and find these results:
* Class Average (using `np.mean`)
* Highest and Lowest grades (using `np.max` and `np.min`)
* Standard Deviation (using `np.std` to see the spread of marks)
* Total passed and failed students count (using conditional array checking)
