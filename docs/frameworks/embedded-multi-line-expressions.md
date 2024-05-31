---
layout: default
title: Embedded and Multi-Line Expressions
parent: Karate
grand_parent: Frameworks
nav_order: 5
---

# Embedded and Multi-Line Expressions

![](/assets/images/karate/embedded-multi-line-expressions.png)

## Embedded Expressions:

- Used to inject dynamic values into requests and other parts of your tests.
- Syntax: `#(object.property)` or `#(variable)`.
- Benefits:
    - Makes tests reusable with unique data for each run.
    - Improves readability by separating data from test logic.

## Multi-Line Expressions:

- Used to define large JSON objects in a readable format.
- Syntax:
    
    ```xml
    request
    """
    {
        "key1": "value1",
        "key2": "#(object.property)"
    }
    """
    ```
    
- Benefits:
    - Enhances readability of tests with complex JSON data.
    - Improves maintainability by separating data from test code.

**Key Takeaways:**

- Use embedded expressions with variables or object properties for dynamic data.
- Use multi-line expressions for defining large, well-formatted JSON objects.
- These techniques improve test maintainability and readability.