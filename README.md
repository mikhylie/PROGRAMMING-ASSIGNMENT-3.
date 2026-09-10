# PROGRAMMING-ASSIGNMENT-3.

###### EXPERIMENT 3 - Python Data Analysis
###### NAME: MARQUEZ, AALIYAH MIKHYLIE L.
###### SECTION: 2ECE-D
###### DATE SUBMITTED: SEPTEMBER 10, 2026

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
2. Load the 'cars.csv' file into a DataFrame named cars
```
  cars = pd.read_csv('cars.csv')
```
### a. Display the shape and complete list of column names of cars.
```
  print("Shape of cars:", cars.shape)
  print("Column names:")
  print(cars.columns.tolist())                         
```
### b. Using positional slicing, create cars 6 to 10 containing rows 6 through 10 of the dataset, where the first data row is row 1.
```
cars_6_to_10 = cars.iloc[5:10]
```

### c. From cars 6 to 10, display only the columns Model, mpg, cyl, hp, and gear, in that order.
```
selected_cars = cars_6_to_10[["Model", "mpg", "cyl", "hp", "gear"]]
selected_cars
```
### **<ins> B. MODEL LOOKUP:</ins>**  
Use Boolean indexing on the Model column to answer both requests.

a. Display the complete row for Toyota Corolla.

b. For Pontiac Firebird, display only Model, mpg, hp, and wt.

Store the two results in toyota and pontiac, respectively. Do not use a hard-coded row number to locate either model.

#### **<ins> IMPLEMENTATION:</ins>**

### a. Display the complete row for Toyota Corolla.
```
toyota = cars[cars["Model"] == "Toyota Corolla"]
toyota
```

### b. For Pontiac Firebird, display only Model, mpg, hp, and wt.
```
pontiac = cars.loc[
    cars["Model"] == "Pontiac Firebird",
    ["Model", "mpg", "hp", "wt"]]
pontiac
```
### **<ins> C. MULTI-MODEL SUBSETTING:</ins>**  
Create a DataFrame named selected_cars containing only the records for three models: Datsun 710, Lotus Europa, and Ferrari Dino.

For these records, retain only Model, mpg, cyl, hp, and gear. Select the rows by their model values rather than by row numbers. Display selected cars and its shape.

Required check: The final DataFrame must contain exactly three rows and five columns.

#### **<ins> IMPLEMENTATION:</ins>**
1. Define the models we want
```
three_models = ["Datsun 710", "Lotus Europa", "Ferrari Dino"]
```
2. Select rows where Model is one of the three, using Boolean indexing
```
selected_cars = cars[cars["Model"].isin(three_models)]
```
3. Keep only the required columns, in the specified order
```
selected_cars = selected_cars[["Model", "mpg", "cyl", "hp", "gear"]]
selected_cars
```
4. Display the result and its shape
```
print("\nShape:", selected_cars.shape)
```
