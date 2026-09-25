# C++ Date Library

A reusable C++ `clsDate` class that provides a collection of functions for working with dates.

The library supports date creation, validation, calendar generation, date arithmetic, date comparison, day-of-week calculations, and business-day operations.

## Features

* Create dates using multiple constructors
* Get the current system date
* Validate dates
* Check leap years
* Calculate the number of days in a month or year
* Calculate hours, minutes, and seconds in months and years
* Determine the day of the week
* Get short names for days and months
* Print monthly and yearly calendars
* Calculate the day order within a year
* Add and subtract:

  * Days
  * Weeks
  * Months
  * Years
  * Decades
  * Centuries
  * Millenniums
* Calculate the difference between two dates
* Compare two dates
* Check whether a date is before, equal to, or after another date
* Check weekends and business days
* Calculate business days between dates
* Calculate vacation days and vacation return dates
* Calculate the user's age in days

## Main Class

```cpp
class clsDate
```

The class stores:

```cpp
Day
Month
Year
```

and provides both object-based and static methods for date operations.

## Examples

### Create a Date

```cpp
clsDate Date1(25, 9, 2026);
Date1.Print();
```

### Get the Current Date

```cpp
clsDate Today = clsDate::GetSystemDate();
Today.Print();
```

### Check if a Date Is Valid

```cpp
clsDate Date1(29, 2, 2024);

if (Date1.IsValid())
    cout << "Valid Date";
else
    cout << "Invalid Date";
```

### Add Days

```cpp
Date1.AddDays(10);
Date1.Print();
```

### Add One Month

```cpp
Date1.IncreaseDateByOneMonth();
Date1.Print();
```

### Compare Dates

```cpp
clsDate Date1(10, 5, 2025);
clsDate Date2(20, 5, 2025);

if (Date1.IsDateBeforeDate2(Date2))
    cout << "Date1 is before Date2";
```

### Calculate Difference Between Dates

```cpp
int Days = clsDate::GetDifferenceInDays(Date1, Date2);

cout << Days << endl;
```

### Print a Month Calendar

```cpp
clsDate::PrintMonthCalendar(9, 2026);
```

### Print a Year Calendar

```cpp
clsDate::PrintYearCalendar(2026);
```

## Project Structure

```text
C++-Date-Library/
│
├── clsDate.h
├── clsString.h
├── main.cpp
└── README.md
```

## Requirements

* C++ compiler
* Standard C++ library
* Visual Studio or another C++ IDE

## Concepts Practiced

This project demonstrates several important C++ concepts:

* Classes and objects
* Constructors
* Static methods
* Encapsulation
* Functions
* References
* Enumerations
* Arrays
* Loops
* Conditional statements
* String handling
* Date and time functions
* Object-oriented programming

## Notes

The implementation uses the Gregorian calendar for leap-year and day-of-week calculations.

The project also includes business-day and vacation calculations based on the weekend rules implemented in the class.

## Credits

The original class structure and learning material are based on programming lessons by Mohammed Abu-Hadhoud / Programming Advices.

This repository is maintained as a learning and C++ programming practice project.
