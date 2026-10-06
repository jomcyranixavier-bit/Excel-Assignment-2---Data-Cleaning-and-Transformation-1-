Steps
-----------
1) Handling Missing Values
    Check for missing values in the 'Price' column. How would you handle products with missing price information?
   Missing valus:COUNTBLANK(H2:H32) 3
   use Median 130 for imputation IF(ISBLANK([@[Price ($)]]),MEDIAN([Price ($)]),[@[Price ($)]])
   • If there are products with missing categories, propose a strategy to impute or deal with these missing values effectively.![Uploading images.png…]()

   Replace the missing category with unknown using CTRL+H
2) Correcting Inconsistent Data:
   Identify any inconsistent text formats present in the "Product Name" column.
   clean(), trim() proper()
•  Identify any typos present in the "Category" column.
   Corrected Electroni as Electrnonics using ctrl+H
   Use the find and replace function to standardize the text formats in the "Product Name" column and fix any typos or misspellings in the "Category" column.

3) Removing Duplicates:
  • Identify any duplicate rows within the dataset based on the entirety of each row, and remove them if any.
Select the entire data set then Data tab-data tools-Removing Dupicates

4) Splitting and Merging Data
  Split the "Product ID" column into two separate columns for " Manufacturing Date" and "Country Code". Remove unnecessary characters, if any.
• Merge the "Brand Name" and "Product Name" columns into one column named "Product Brand".
[@[New Product ]] & " " & [@[Brand Name]]

5) Number Formatting:
 • Format the data type of the "Price" column to currency format.
Right clicK-Format cells-choose currency
 Format the "Manufacturing Date" column to display dates in the "DD-MM-YYYY " format.
A2 & "2026"

6) Conditional Formatting
 • Apply data bar or color scales conditional formatting in the "Price" column.
• Create a custom rule for conditional formatting in the "Category" column to highlight cells where the category is "Electronics."
