Create a function called finalGrade, which outputs the final grade of a student depending on two parameters: a grade for the exam and a number of completed projects.
Create a function called finalGrade, which outputs the final grade of a student depending on two parameters: a grade for the exam and a number of completed projects.

This function should take two arguments: exam - grade for exam (from 0 to 100); projects - number of completed projects (from 0 and above);

This function should `return` a number (final grade). There are four types of final grades:

-   100, if a grade for the exam is more than 90 or if a number of completed projects more than 10.
-   90, if a grade for the exam is more than 75 and if a number of completed projects is minimum 5.
-   75, if a grade for the exam is more than 50 and if a number of completed projects is minimum 2.
-   0, in other cases

The user will input his grade for exam and number of completed project. The final grade is the output.

Sample Output
```
Exam Grade: 100
Projects Completed: 12 
Final Grade: 100
```

```
Exam Grade: 85
Projects Completed: 5
Final Grade: 90
```

```
Exam Grade: 55
Projects Completed: 3
Final Grade: 75
```

```
Exam Grade: 55
Projects Completed: 0
Final Grade: 0
```

# My Answer

```python
def final_grade(exam, projects):
    if exam > 90 or projects > 10:
        return 100
    elif exam > 75 and projects > 4:
        return 90
    elif exam > 50 and projects > 1:
        return 75
    else:
        return 0

exam = int(input("Exam Grade: "))
projects = int(input("Projects Completed: "))
finalGrade = final_grade(exam, projects)

print(f"Final Grade: {finalGrade}")
```
