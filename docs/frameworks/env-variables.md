---
layout: default
title: Environment Variables
parent: Karate
grand_parent: Frameworks
nav_order: 5
---

# Environment Variables

**Environment Variables in Karate Framework:**

- Used to store global variables accessible across all feature files.
- Useful for managing reusable data like URLs, credentials, etc.
- Kept in a separate file named `karate-config.js`.

**Benefits of Environment Variables:**

- Avoids code duplication by storing reusable data in one place.
- Enables easy switching between environments (dev, QA, etc.) by changing a single flag.
- Improves code maintainability and reduces errors.

## karate-config.js

![](/assets/images/karate/env-1.png)

Add token to configuration file.

![](/assets/images/karate/env-2.png)

**Switching Environments:**

- Use `mvn test -DargLine="-Dkarate.env=<environment_name>"` flag during test execution (e.g., `mvn test -DargLine="-Dkarate.env=test"`).