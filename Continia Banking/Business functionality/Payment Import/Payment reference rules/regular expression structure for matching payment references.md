---
title: Regular expression structure for matching payment references
description: Learn how to use regular expressions to match and validate structured payment reference formats like FIK and SCOR in Business Central.
date: 07-07-2025
id: CB-254
lang: en
---

# Regular expression structure for matching payment references

A regular expression (regex) is a sequence of characters that defines a specific pattern used to search patterns in text. Regex is commonly used for pattern matching, input validation, text transformation, and querying. When working with payment references in Business Central, regular expressions help define and validate the structure of the incoming reference strings. This is especially useful when dealing with various standardized formats such as **FIK** or **SCOR** references.

This article describes how these regular expressions work and what each part does.

## Example 1: FIK reference

The following example provides a pattern that matches the references exactly.

**Sample string:** 

`71/000000001032259`

**Regex pattern:**

`^71\/(?!0{14})\d{14}\d$`

**Explanation:**

| Pattern     | Description                                                  |
| ----------- | ------------------------------------------------------------ |
| `^`         | Anchors the expression to the start of the string.           |
| `71/`       | Matches the literal prefix `71/`, which is fixed.            |
| `(?!0{14})` | A negative lookahead that ensures the next 14 characters are not all zeroes. |
| `\d{14}`    | Matches exactly 14 digits.                                   |
| `\d`        | Matches one additional digit, usually a check digit.         |
| `$`         | Anchors the expression to the end of the string.             |

This pattern ensures:

- The reference starts with `71/`.
- The main body isn’t all zeroes.
- The total number of digits after the slash is **15**.
- The string matches the expected structure exactly - no more, no less.

## Example 2: SCOR reference

The SCOR reference begins with `RF`, followed by 2 digits, then up to 21 alphanumeric characters. The following pattern enforces the required `RF` prefix and check digits, and allows a flexible range of characters afterward.

**Sample string**: 

RF18539007547034

**Regex pattern:**

```
^RF\d{2}[0-9A-Za-z]{1,21}$
```

**Explanation:**

| Pattern             | Description                                                  |
| ------------------- | ------------------------------------------------------------ |
| `^`                 | Anchors the expression to the start of the string.           |
| `RF`                | Matches the literal characters *RF*.                         |
| `\d{2}`             | Matches exactly 2 digits.                                    |
| `[0-9A-Za-z]{1,21}` | Matches between 1 and 21 alphanumeric characters (digits and letters, upper or lowercase). |
| `$`                 | Anchors the expression to the end of the string.             |

This pattern allows flexible but valid SCOR references by:
- Requiring the `RF` prefix and 2 check digits.
- Allowing a wide range of characters afterward.
- Limiting the length to a maximum of 21 characters.
