## repo: https://github.com/TexanInParis/Effective-SQL/tree/master/MySQL


## 🧁 Chapter 1: Data Model Design (11)
#### Item 1: Verify That All Tables Have a Primary Key (11)
#### Item 2: Eliminate Redundant Storage of Data #### Items (15)
#### Item 3: Get Rid of Repeating Groups (19)
#### Item 4: Store Only One Property per Column (21)
#### Item 5: Understand Why Storing Calculated Data Is Usually a Bad Idea (25)
#### Item 6: Define Foreign Keys to Protect Referential Integrity (30)
#### Item 7: Be Sure Your Table Relationships Make Sense (33)
#### Item 8: When 3NF Is Not Enough, Normalize More (37)
#### Item 9: Use Denormalization for Information Warehouses (43)

## 🍰 Chapter 2: Programmability and Index Design (47)
#### Item 10: Factor in Nulls When Creating Indexes (47)
#### Item 11: Carefully Consider Creation of Indexes to Minimize Index and Data Scanning (52)
#### Item 12: Use Indexes for More than Just Filtering (56)
#### Item 13: Don’t Go Overboard with Triggers (61)
#### Item 14: Consider Using a Filtered Index to Include or Exclude a Subset of Data (65)
#### Item 15: Use Declarative Constraints Instead of Programming Checks (68)
#### Item 16: Know Which SQL Dialect Your Product Uses and Write Accordingly (70)
#### Item 17: Know When to Use Calculated Results in Indexes (74)

## 🌵 Chapter 3: When You Can’t Change the Design (79)
#### Item 18: Use Views to Simplify What Cannot Be Changed (79)
#### Item 19: Use ETL to Turn Nonrelational Data into Information (85)
#### Item 20: Create Summary Tables and Maintain Them (90)
#### Item 21: Use UNION Statements to “Unpivot” Non-normalized Data (94)

## 👓 Chapter 4: Filtering and Finding Data (101)
#### Item 22: Understand Relational Algebra and How It Is Implemented in SQL (101)
#### Item 23: Find Non-matches or Missing Records (108)
#### Item 24: Know When to Use CASE to Solve a Problem (110)
#### Item 25: Know Techniques to Solve Multiple-Criteria Problems (115)
#### Item 26: Divide Your Data If You Need a Perfect Match (120)
#### Item 27: Know How to Correctly Filter a Range of Dates on a Column Containing Both Date and Time (124)
#### Item 28: Write Sargable Queries to Ensure That the Engine Will Use Indexes (127)
#### Item 29: Correctly Filter the “Right” Side of a “Left” Join (132)

## 🗡️ Chapter 5: Aggregation (135)
#### Item 30: Understand How GROUP BY Works (135)
#### Item 31: Keep the GROUP BY Clause Small (142)
#### Item 32: Leverage GROUP BY/HAVING to Solve Complex Problems (145)
#### Item 33: Find Maximum or Minimum Values Without Using GROUP BY (150)
#### Item 34: Avoid Getting an Erroneous COUNT() When Using OUTER JOIN (156)
#### Item 35: Include Zero-Value Rows When Testing for HAVING COUNT(x) < Some Number (159)
#### Item 36: Use DISTINCT to Get Distinct Counts (163)
#### Item 37: Know How to Use Window Functions (166)
#### Item 38: Create Row Numbers and Rank a Row over Other Rows (169)
#### Item 39: Create a Moving Aggregate (172)

## 🌞 Chapter 6: Subqueries (179)
#### Item 40: Know Where You Can Use Subqueries (179)
#### Item 41: Know the Difference between Correlated and Non-correlated Subqueries (184)
#### Item 42: If Possible, Use Common Table Expressions Instead of Subqueries (190)
#### Item 43: Create More Efficient Queries Using Joins Rather than Subqueries (197)

## ⛑️ Chapter 7: Getting and Analyzing Metadata (201)
#### Item 44: Learn to Use Your System’s Query Analyzer (201)
#### Item 45: Learn to Get Metadata about Your Database (212)
#### Item 46: Understand How the Execution Plan Works (217)

## 📽️ Chapter 8: Cartesian Products (227)
#### Item 47: Produce Combinations of Rows between Two Tables and Flag Rows in the Second That Indirectly Relate to the First (227)
#### Item 48: Understand How to Rank Rows by Equal Quantiles (231)
#### Item 49: Know How to Pair Rows in a Table with All Other Rows (235)
#### Item 50: Understand How to List Categories and the Count of First, Second, or Third Preferences (240)

## ⛲ Chapter 9: Tally Tables (247)
#### Item 51: Use a Tally Table to Generate Null Rows Based on a Parameter (247)
#### Item 52: Use a Tally Table and Window Functions for Sequencing (252)
#### Item 53: Generate Multiple Rows Based on Range Values in a Tally Table (257)
#### Item 54: Convert a Value in One Table Based on a Range of Values in a Tally Table (261)
#### Item 55: Use a Date Table to Simplify Date Calculation (268)
#### Item 56: Create an Appointment Calendar Table with All Dates Enumerated in a Range (275)
#### Item 57: Pivot Data Using a Tally Table (278)

## 🌴 Chapter 10: Modeling Hierarchical Data (285)
#### Item 58: Use an Adjacency List Model as the Starting Point (286)
#### Item 59: Use Nested Sets for Fast Querying Performance with Infrequent Updates (288)
#### Item 60: Use a Materialized Path for Simple Setup and Limited Searching (291)
#### Item 61: Use Ancestry Traversal Closure for Complex Searching 294