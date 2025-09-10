
Suppose your Name values are in column A (starting from cell A2):

In cell B2, enter:

=A2 & "@gmail.com"


Explanation:

& is used to concatenate (join) text.

So if A2 contains john, the formula will return john@gmail.com.

👉 If you want to apply it to the whole column, just drag the formula down.

without that i wanna remove my formula looks like not used what should i do?
Select the column (or cells) that have the formulas.

Copy them (Ctrl + C).

Right-click on the same selection.

Under Paste Options, click Values (icon with 123).


tell me about Vlookup and pivot table:
🔍 VLOOKUP

Use case: Look up a value in a table and return related information.
Think of it as: "Find this thing in the first column, then bring me something from another column in the same row."

=VLOOKUP(lookup_value, table_array, col_index_num, [range_lookup])

-lookup_value → the value you want to search for

-table_array → the table (range of cells) where to search

-col_index_num → column number in the table to return from (1 = first column, 2 = second, etc.)

-range_lookup → FALSE for exact match (most common), TRUE for approximate

Example:

| A (ID) | B (Name) | C (Salary) |
| ------ | -------- | ---------- |
| 101    | Alice    | 5000       |
| 102    | Bob      | 6000       |
| 103    | Charlie  | 7000       |



Formula:
=VLOOKUP(102, A2:C4, 3, FALSE)


📊 Pivot Table

Use case: Summarize, analyze, and organize large datasets quickly.
Think of it as: "Drag and drop fields to get instant reports, totals, and insights."

What it can do:

Sum, average, count, min, max

Group data by rows/columns

Easily compare categories

Filter large datasets

Example:

Imagine this dataset:
| Product | Region | Sales |
| ------- | ------ | ----- |
| Laptop  | East   | 2000  |
| Laptop  | West   | 3000  |
| Phone   | East   | 1500  |
| Phone   | West   | 2500  |

Using a Pivot Table, you can drag:

Product → Rows

Region → Columns

Sales → Values (SUM)

👉 Instantly get:

| Product | East | West | Total |
| ------- | ---- | ---- | ----- |
| Laptop  | 2000 | 3000 | 5000  |
| Phone   | 1500 | 2500 | 4000  |

