# Python Exercise 1

Lecture date: 28.10.2026

## Task
Copy the code below into a single code cell in a Colab Python Notebook and complete the missing parts according to the instructions.

## About Comment Lines
Some lines start with a comment marker so that the code can be executed without errors while progressing step by step. These lines are marked with `# Remove comment marker`. Example:

```
# message = "This line is commented out"  # Remove comment marker
# print(message)                           # Remove comment marker
```
And when you progress to that line in the exercise, simply remove the comment marker so the line becomes active and the output appears, i.e.
```
message = "This line is commented out"  # Remove comment marker
print(message)                           # Remove comment marker
```

## Code to Complete

```
# -----------
# 1. Practice the basics of number handling
# Complete the sum, difference, and product of numbers a and b
a = 10
b = 3

#sum =         # Remove comment marker
#difference =  # Remove comment marker
#product =     # Remove comment marker

#print("Sum:", sum)                # Remove comment marker
#print("Difference:", difference)  # Remove comment marker
#print("Product:", product)        # Remove comment marker

# -----------
# 2. Complete the variables. Name is a string and age is a number
name = ""
age = 0

# -----------
# 3. Print a greeting by adding the name after the comma
# print("Hi", )

# -----------
# 4. Calculate how many leap years you have lived
# No changes needed in this section
year_now = 2026
birth_year = year_now - age

leap_years = 0

for year in range(birth_year, year_now + 1):
    if (year % 4 == 0 and year % 100 != 0) or (year % 400 == 0):
        leap_years += 1

print("Leap years in your life:", leap_years)

# -----------
# 5. Now we can calculate how many days old the person is, i.e., multiply age
# by the number of days in a regular year (365) and add the number of leap days

# age_in_days =            # Remove comment marker
# print("Age in days:", )  # Remove comment marker

# -----------
# 6. Let's explore tables as a data structure. Complete the print lines below 
# with the calculated sums and averages of the columns
# The import command allows us to bring certain pre-made code collections into 
# our own program. These are called libraries. We use the pandas library here 
# and shorten its name to pd
import pandas as pd

# Create an example table of size 10 x 2
table = [
    [5, 8],
    [3, 7],
    [6, 4],
    [9, 2],
    [1, 5],
    [4, 6],
    [8, 3],
    [2, 9],
    [7, 1],
    [5, 4]
]

# Convert to DataFrame (pandas library's name for a certain type of table),
# where the column names are Temperature and Rainfall
df = pd.DataFrame(table, columns=["Temperature", "Rainfall"])

# Print the table to display it
display(df)

# Calculate column sums using the pandas library
sum1 = df["Temperature"].sum()
sum2 = df["Rainfall"].sum()

# Calculate column averages using the pandas library
avg1 = df["Temperature"].mean()
avg2 = df["Rainfall"].mean()

#print("Temperature sum:", )  # Remove comment marker
#print("Rainfall sum:", )     # Remove comment marker

#print("Temperature average:", )  # Remove comment marker
#print("Rainfall average:", )     # Remove comment marker

# -----------
# 7. The golden ratio is a point on a line segment that divides it such that 
# the ratio of the longer part's length to the whole line's length is the same 
# as the ratio of the shorter part's length to the longer part's length. 
# Ask AI to create code with which you can calculate the golden ratio division 
# for a line segment of any length and copy the code below here.
```


[Back to lecture notes](Lectures.md)
