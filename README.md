Name:Pranita Dnyaneshwar Tupe
Company:CODETECH IT SOLUTIONS
ID:CT08DS6343
Domain:Python Programming
Duration:August to September 2024
Mentor:Muzammil Ahmed

Overview of the project

Here's an overview of a Python program project to calculate the average of grades:

Project Title: Grade Average Calculator

Objective: Create a Python program that calculates the average of a set of grades input by the user.

Features:

1. User input: Allow the user to enter a set of grades (e.g., 85, 90, 78, etc.)
2. Grade storage: Store the input grades in a list or array
3. Average calculation: Calculate the average of the grades using a formula (sum of grades / number of grades)
4. Output: Display the average grade to the user

Example Code:

# Get user input for grades
grades = input("Enter grades (separated by spaces): ")
grades_list = [float(grade) for grade in grades.split()]

# Calculate average grade
average_grade = sum(grades_list) / len(grades_list)

# Display average grade
print("Average grade:", average_grade)

Enhancements:

1. Error handling: Add try-except blocks to handle invalid user input (e.g., non-numeric grades)
2. Grade validation: Check if grades are within a valid range (e.g., 0-100)
3. Multiple datasets: Allow the user to input multiple sets of grades and calculate averages for each set
4. Grade distribution: Display a distribution of grades (e.g., histogram, bar chart)

Program:
def calculate_average(grades):
    """Calculate the average of the given grades."""
    return sum(grades) / len(grades) if grades else 0

def get_letter_grade(average):
    """Convert the average grade to a letter grade."""
    if average >= 90:
        return 'A'
    elif average >= 80:
        return 'B'
    elif average >= 70:
        return 'C'
    elif average >= 60:
        return 'D'
    else:
        return 'F'

def calculate_gpa(average):
    """Calculate GPA based on the average grade."""
    if average >= 90:
        return 4.0
    elif average >= 80:
        return 3.0
    elif average >= 70:
        return 2.0
    elif average >= 60:
        return 1.0
    else:
        return 0.0

def main():
    grades = []
    
    print("Welcome to the Grade Tracker")
    
    while True:
        try:
            grade = float(input("Enter a grade (or type 'done' to finish): "))
            grades.append(grade)
        except ValueError:
            if input("Finished entering grades? (y/n): ").lower() == 'y':
                break
            else:
                print("Invalid input. Please enter a numeric grade.")
    
    if grades:
        average = calculate_average(grades)
        letter_grade = get_letter_grade(average)
        gpa = calculate_gpa(average)

        print("\nFinal Results:")
        print(f"Average Grade: {average:.2f}")
        print(f"Letter Grade: {letter_grade}")
        print(f"GPA: {gpa:.2f}")
    else:
        print("No grades entered.")

if _name_ == "_main_":
    main()

Output:
C:\Users\Pranita\PycharmProjects\pythonProject7\.venv\Scripts\python.exe C:\Users\Pranita\PycharmProjects\pythonProject7\main.py 
Welcome to the Grade Tracker
Enter a grade (or type 'done' to finish): 50
Enter a grade (or type 'done' to finish): 70
Enter a grade (or type 'done' to finish): 90
Enter a grade (or type 'done' to finish): 59
Enter a grade (or type 'done' to finish): 89
Enter a grade (or type 'done' to finish): y
Finished entering grades? (y/n): y

Final Results:
Average Grade: 71.60
Letter Grade: C
GPA: 2.00

Process finished with exit code 0

Skills Demonstrated:

1. User input and output
2. Data storage and manipulation (lists/arrays)
3. Basic calculations (sum, average)
4. Error handling and validation

This project is great for beginners to practice fundamental Python concepts and build a useful tool for students or educators.
