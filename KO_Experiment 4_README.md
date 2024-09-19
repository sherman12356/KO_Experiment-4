# Experiment 4: Data Wrangling and Data Visualization

## I. Intended Learning Outcomes
1. to determine the functions and codes required for data cleaning and visualization.
2. to employ several codes and functions while developing a Python program for data visualization and wrangling.

## II. Instructions
Write a Python script in a Jupyter Notebook to perform the following tasks. Submit your notebook via the designated submission platform.

### Dataset:
Download the ECE Board Exam 2 dataset from [Board2_xlsx](http://bit.ly/ECEBoardExamDataset).

### ECE Board Exam Problem:
Using **data wrangling** and **data visualization** techniques with storytelling, analyze the dataset and present:


### 1. 
Create the following data frames based on the format provided:

Example: Vis = [“Name”, “Gender”, “Track”, “Math<70”]; hometown is constant as **Visayas** 

Output:

| Name | Gender | Track          | Math |
|------|--------|----------------|------|
| S4   | Male   | Instrumentation | 65   |
| S11  | Female | Communication   | 48   |
| S22  | Female | Communication   | 64   |

#### a. 
Create the follwing DataFrame:
- **Instructions**
  1. Sort the Data Frame as Instru = [“Name”, “Gender”, “Track”, “Math<70”];  
  2. Where Track is constant as Instrumentation and hometown is Luzon
  3. Save it as Instru
#### b.
Create the following Datafame:
- **Instructions**
  1. Sort the DataFrame as Mindy = [“Name”, “Track”, “Electronics”, “Average >=55”]
  2. Where Hometown is constant as Mindanao and gender is Female
  3. Save it as Mindy

 ### 2. 
  - Create visualizations that show how the following features contribute to the average grade:
    1. Chosen track in college
    2. Gender
    3. Hometown

## III. Setup Instructions:

### 1. Install Required Libraries:
Ensure you have Python,Pandas, Matplotlib and seaborn installed.
### 2. Running the Code:
After completing each problem, run your Python script in Jupyter Notebook or from the command line. 

## IV. Submission:
 Submit your Jupyter Notebook in the dedicated submission folder before the deadline.
 Make sure your code is well-commented and follows the instructions closely.

 ## Example Output:
```python
import pandas as pd

#read the board_excel file.
board=pd.read_excel('board2.xlsx')

#Sort the board to track only data where 'Track' is Instrumentation and 'Hometown' is Luzon.
instru=board[(board['Track'] == 'Instrumentation') & (board['Hometown'] == 'Luzon')]

#Sort the board again to only show data where the 'Electronics' is greater than 70. It will only preview the 'Name','GEAS', and'Electronics'.
instru=instru.loc[(instru['Electronics']>70),['Name','GEAS','Electronics']]

# save the DataFrame  as an excel file and name it 'Instru'
instru.to_excel('Instru.xlsx',index=False)

  ```
## VI. HIstory:
- V1 : intial code for part 1 a
- V2 : intial code for part 1 b
- V3 : added markdowns and finished the code for part 1
- V4 : initial code for part 2
- V5 : added markdowns and finished the code for part 1
- V6 : Fixed the in line comments
