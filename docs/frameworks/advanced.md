---
layout: default
title: Advanced
parent: Karate
grand_parent: Frameworks
nav_order: 4
---

{: .no_toc }

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
- TOC
{:toc}
</details>

## Data Driven

![](/assets/images/data-driven.png)

Key takeaways:

- Use scenario outlines when you need to run the same test with different data sets.
- Scenario outlines have an examples section that defines test data columns.
- You can reference these columns within your test steps using angle braces.
- This approach improves code maintainability and reduces redundancy.

## Debugging

**Common Mistakes:**

- Typos in commands (e.g., "users" misspelled)
- Incorrect syntax (e.g., "match response" instead of "match response")
- Incorrect use of operators (e.g., "=" for assertion instead of "==")
- Mistakes in file paths (e.g., misspelling a helper file name)
- Java class not found errors
- Misspelled variable names
- Missing double quotes in embedded expressions

**Debugging Strategies:**

- **Run tests often:** After small changes, run tests to identify issues early.
- **Read error messages carefully:** Understand the error messages and trace them back to the source.
- **Narrow down the scope:** Comment out code sections to isolate the error.
- **Use** `print` command: Print variable values to the console for inspection.
- **Copy-paste environment variables:** Reduce mistakes by copying environment variables from `karate-config.js` to feature files.

**Debugging Specific Scenarios:**

- **Missing line number in error message:** Comment out code sections to isolate the error line.
- **Error originating outside feature files (data generator):** Check for errors in the data generator file using syntax highlighting.
- **Error in** `karate-config.js`: Identify the error line by commenting out sections and observing build success. Consider copying environment variables to feature files.

**Additional Tips:**

- Keep `karate-config.js` small and simple.
- Don't be afraid of error messages.
- Read error messages from bottom to top.
- Narrow down the scope by commenting out code.
- Use `print` for variable value inspection.