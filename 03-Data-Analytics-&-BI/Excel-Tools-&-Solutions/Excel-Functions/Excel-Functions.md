# Excel Functions

A practical collection of Microsoft Excel functions with syntax, explanations, examples, and real-world business applications.

## Overview

This section documents commonly used and advanced Microsoft Excel functions that help simplify calculations, automate data processing, perform logical operations, retrieve information, and analyze business data.

The objective is to provide practical examples and reusable function solutions for everyday spreadsheet operations as well as complex business requirements.

## Function Categories

| Category | Description | Example Functions |
|---|---|---|
| Mathematical & Statistical | Mathematical calculations and statistical analysis. | `SUM`, `SUMIF`, `SUMIFS`, `AVERAGE`, `COUNT`, `COUNTIF`, `MAX`, `MIN` |
| Logical | Conditional calculations and decision-making. | `IF`, `IFS`, `AND`, `OR`, `NOT`, `IFERROR`, `SWITCH` |
| Lookup & Reference | Searching and retrieving data from tables and ranges. | `VLOOKUP`, `HLOOKUP`, `XLOOKUP`, `INDEX`, `MATCH`, `XMATCH` |
| Text | Extracting, combining, and manipulating text. | `LEFT`, `RIGHT`, `MID`, `LEN`, `TRIM`, `CONCAT`, `TEXTJOIN`, `SUBSTITUTE` |
| Date & Time | Date calculations and time-based analysis. | `TODAY`, `NOW`, `DATE`, `DAY`, `MONTH`, `YEAR`, `DATEDIF`, `EOMONTH` |
| Dynamic Array | Working with dynamic data ranges and array results. | `FILTER`, `SORT`, `SORTBY`, `UNIQUE`, `SEQUENCE`, `TAKE`, `DROP` |
| Financial | Financial calculations and investment analysis. | `PMT`, `PV`, `FV`, `NPV`, `IRR`, `RATE` |
| Information | Checking cell contents, data types, and errors. | `ISBLANK`, `ISNUMBER`, `ISTEXT`, `ISERROR`, `ISNA`, `CELL` |
| Database | Conditional calculations using database-style criteria. | `DSUM`, `DCOUNT`, `DAVERAGE`, `DMAX`, `DMIN` |

*Function availability may vary depending on the Microsoft Excel version.*

## Function Documentation Format

Each documented function may include the following information:

- **Function Name:** Official Excel function name.
- **Category:** Functional classification.
- **Purpose:** What the function does.
- **Syntax:** Correct formula structure.
- **Arguments:** Explanation of required and optional parameters.
- **Practical Example:** A working Excel formula.
- **Expected Result:** Explanation of the output.
- **Business Application:** How the function can solve real-world problems.

## Practical Examples

### 1. SUMIFS

**Purpose:** Calculates the sum of values that meet multiple criteria.

**Syntax:**

```excel
=SUMIFS(sum_range, criteria_range1, criteria1, [criteria_range2, criteria2], ...)
```

**Example:**

```excel
=SUMIFS(D2:D100, B2:B100, "Buyer A", C2:C100, "January")
```

**Business Application:** Calculate total order quantity for a specific buyer and month.

### 2. XLOOKUP

**Purpose:** Searches a range or array and returns a corresponding value.

**Syntax:**

```excel
=XLOOKUP(lookup_value, lookup_array, return_array, [if_not_found], [match_mode], [search_mode])
```

**Example:**

```excel
=XLOOKUP(A2, Employee_ID, Employee_Name, "Not Found")
```

**Business Application:** Retrieve employee names, buyer information, product details, or order references.

### 3. IFERROR

**Purpose:** Returns an alternative result when a formula produces an error.

**Syntax:**

```excel
=IFERROR(value, value_if_error)
```

**Example:**

```excel
=IFERROR(A2/B2, 0)
```

**Business Application:** Prevent error messages in reports when calculations involve missing or invalid data.

### 4. FILTER

**Purpose:** Returns records that satisfy specified conditions.

**Syntax:**

```excel
=FILTER(array, include, [if_empty])
```

**Example:**

```excel
=FILTER(A2:D100, B2:B100="Buyer A", "No Records Found")
```

**Business Application:** Dynamically display all records belonging to a particular buyer.

## Practical Business Applications

Excel functions can be combined to develop solutions for:

- Buyer-wise order and booking calculations.
- Monthly production and capacity analysis.
- Employee attendance and working-hour calculations.
- Conditional business reporting.
- Automated data retrieval and reconciliation.
- Inventory and stock calculations.
- Dynamic MIS reports.
- Business performance and KPI analysis.

## Learning & Development

This section will progressively include:

1. Basic Excel Functions
2. Intermediate Excel Functions
3. Advanced Excel Functions
4. Dynamic Array Functions
5. Complex Formula Combinations
6. Real-world Business Formula Solutions

## Notes

- All examples are intended for practical learning and implementation.
- Formula separators may differ depending on regional Excel settings.
- Some functions require Microsoft 365 or newer Excel versions.
- Sample data and expected outputs will be provided where applicable.

---

**Author:** Md Tawhidul Islam  
**GitHub:** [@tawhidna](https://github.com/tawhidna)

**Main Repository:** [My Project Showcase](https://github.com/tawhidna/my-project-showcase)

*Practical Excel Functions for Smarter Calculations and Better Business Decisions.*
