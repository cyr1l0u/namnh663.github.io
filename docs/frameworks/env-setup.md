---
layout: default
title: Env Setup
parent: Karate
grand_parent: Frameworks
nav_order: 2
---

# Required Dependencies

- Java 21
- Maven 3
- Git
- Postman API testing tool
- Visual Studio Code
- Visual Studio Code extensions:
    - Cucumber - Gherkin Full Support
    - Karate Runner
    - Java Extension Pack
    - Open In Default Browser

# Install the dependencies on Windows

**Java:**

1. Go to the Oracle website https://www.oracle.com/java/technologies/downloads/.
2. Download Java 21.
3. Click on the JDK download for Windows.
4. Accept the license agreement and download the installer.
5. You might need to create an Oracle account to download the file.
6. Run the downloaded installer and follow the on-screen instructions.

**Maven:** https://www.baeldung.com/install-maven-on-windows-linux-mac.

**Git:**

1. Go to the Git website https://git-scm.com/downloads.
2. Download the latest version for Windows.
3. Run the downloaded installer and follow the on-screen instructions.

**Postman:**

1. Go to the Postman website https://www.postman.com/downloads/.
2. Download the Windows installer and run it.

**Visual Studio Code:**

1. Go to the Visual Studio Code website https://code.visualstudio.com/#alt-downloads.
2. Download the Windows version and install it.

**Visual Studio Code Extensions:**

1. Open Visual Studio Code.
2. Click on the Extensions icon (looks like a box) on the left sidebar.
3. Search for and install the following extensions:
    - Cucumber - Gherkin Full Support
    - Karate Runner
    - Java Extension Pack (make sure to NOT install Java Test Runner)
    - Open In Default Browser

**Verification:**

- Open a command prompt window and type `java -version`. You should see the Java version.
- Type `mvn -v`. You should see information about the installed Maven version.