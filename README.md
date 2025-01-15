# COBOL Data Type Handling Bug

This repository demonstrates a common yet subtle bug in COBOL programs that involves improper handling of data types during arithmetic operations.  The code calculates a tax amount, but due to implicit type conversions, the result can be incorrect. 
The `bug.cob` file contains the erroneous code.  The solution, demonstrating the correct handling of data types, is in `bugSolution.cob`.

## Bug Description

The primary issue stems from the potential loss of precision during arithmetic operations between numeric fields with differing decimal positions. The program calculates a tax amount by multiplying an amount (with two decimal places) and a tax rate (with two decimal places). The result might not accurately reflect the correct tax due to limitations in handling decimal positions. 

## Solution

The solution involves explicitly defining the data types to ensure proper precision during calculations and avoid potential truncation errors.  The corrected code uses data types that can precisely handle the decimal places needed for tax calculations.