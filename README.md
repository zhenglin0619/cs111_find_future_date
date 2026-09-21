# Find Future Date

A small Python `Date` class for working with calendar dates. It stores a month, day, and year, and includes methods for advancing a date, checking leap years, counting days between dates, and finding the day of the week.

This project was created for Computer Science 111.

## Requirements

- Python 3
- No third-party packages

## Usage

The repository provides a class, not an interactive command-line program. Run the following from the repository directory:

```python
from runpy import run_path

Date = run_path("Find Future Date.py")["Date"]

date = Date(8, 6, 2025)  # month, day, year
print(date)               # 08/06/2025
print(date.day_name())    # Wednesday

tomorrow = date.copy()
tomorrow.advance_one()
print(tomorrow)           # 08/07/2025
```

The filename contains spaces, so it cannot be used in a normal `import` statement. You can also rename your own copy to `find_future_date.py` and use `from find_future_date import Date`.

## Methods

| Method | Description |
| --- | --- |
| `Date(month, day, year)` | Create a date. |
| `day_name()` | Return the weekday name. |
| `is_leap_year()` | Check whether the year is a leap year. |
| `days_in_month()` | Return the number of days in the month. |
| `copy()` | Return a separate copy of the date. |
| `advance_one()` | Move the date forward by one day, changing the object. |
| `is_before(other)` / `is_after(other)` | Compare two dates. |
| `days_between(other)` | Return the signed number of days from `other` to this date. |

Dates display in `MM/DD/YYYY` format.

## Current limitations

- The constructor does not validate dates. Pass valid month, day, and year values.
- `is_before()` and `is_after()` can give incorrect results for some dates with different months or years. Since `days_between()` and `day_name()` depend on date comparison, they can also give incorrect results or fail to finish for some inputs.

## License

Licensed under the [Apache License 2.0](LICENSE).
