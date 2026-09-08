# PROGRAMMING-ASSIGNMENT-3.

###### EXPERIMENT 3 - Python Data Analysis
###### NAME: MARQUEZ, AALIYAH MIKHYLIE L.
###### SECTION: 2ECE-D
###### DATE SUBMITTED: SEPTEMBER 9, 2026

#### **<ins> OBJECTIVE:</ins>**
To practice core pandas operations for loading, inspecting, and subsetting tabular data. This exercise demonstrates how to examine a DataFrame’s structure, extract specific rows using iloc and Boolean indexing, and select or reorder columns by label—building foundational skills for data analysis in Python.

### **<ins> A. POSITIONAL AND LABEL-BASED SLICING:</ins>**  
After loading cars, complete the following operations.

a. Display the shape and complete list of column names of cars.

b. Using positional slicing, create cars 6 to 10 containing rows 6 through 10 of the dataset, where
the first data row is row 1.

c. From cars 6 to 10, display only the columns Model, mpg, cyl, hp, and gear, in that order.

Requirement: The row selection in part (b) must use iloc; the column selection in part (c) must
use column labels

#### **<ins> IMPLEMENTATION:</ins>**
1. Import PANDAS library
```
  import pandas as pd                           
```
### a. Load the corresponding .csv file into a data frame named cars using pandas.
2. Load the 'cars.csv' file into a DataFrame named cars
```
  cars = pd.read_csv('cars.csv')
```

