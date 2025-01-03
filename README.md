# Objective-C NSDateFormatter Bug

This repository demonstrates a common bug related to the use of `NSDateFormatter` in Objective-C.  Specifically, it showcases the problems that can arise from using ambiguous date formats and the lack of error handling when parsing dates.

The `dateBug.m` file contains code that demonstrates the issues. The `dateBugSolution.m` file shows the corrected code with proper error handling and a more robust approach to date formatting.

## Bug Description

Using an ambiguous date format (like "MM/dd/yyyy") can lead to unexpected results depending on the user's locale settings.  Failure to check the return value of `dateFromString:` can result in crashes when the parsing fails.

## Solution

The solution involves using a more unambiguous date format and explicitly checking the return value of `dateFromString:` before using the parsed date.  It's recommended to use ISO 8601 format for consistency and clarity.