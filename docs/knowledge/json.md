---
layout: default
title: JSON
parent: API Testing
grand_parent: Knowledge
nav_order: 6
---

# The basics of JSON

**Key Points:**

- **JSON Structure:**
    - Objects: Enclosed in curly braces `{}` and contain key-value pairs. Keys are unique and strings (in double quotes). Values can be any data type.
    - Arrays: Enclosed in square brackets `[]` and are ordered lists of values. Values can be any data type.
- **Data Types:**
    - String: Text data in double quotes (e.g., "John").
    - Number: Numeric data without quotes (e.g., 36).
    - Boolean: `true` or `false`.
    - Null: Represents the absence of a value.
- **Manipulating JSON Data:**
    - Karate uses JsonPath expressions to access and modify JSON data.
    - Access values using dot notation (`.`) and key names.
    - Access elements in arrays using square brackets `[]` and their index (starts from 0).
    - Update values using `set` keyword followed by the path and new value.
    - Add new key-value pairs or elements in arrays using `set` keyword.
    - Remove key-value pairs or elements in arrays using `remove` keyword (only in Karate script).
- **Karate's JSON Support:**
    - Karate natively supports JSON, allowing easy manipulation with JsonPath expressions.

**Example of Manipulating JSON Data with Karate**

```xml
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 36,
  "cars": ["Honda", "BMW"],
  "income": {
    "Q1": "$10,000",
    "Q2": "$20,000"
  },
  "pets": [
    {"type": "dog", "name": "Jimmy"},
    {"type": "cat", "name": "Lisa"}
  ]
}
```

Accessing Data:

- Get John's last name:

```xml
def LastName = myObject.lastName
```

- Get the second car:

```xml
def secondCar = myObject.cars[1]
```

- Get income for Q2:

```xml
q2Income = myObject.income.Q2
```

- Get the type of the first pet:

```xml
firstPetType = myObject.pets[0].type
```

Updating Data:

- Update John's age to 40:

```xml
set myObject.age = 40
```

- Change the cat's name to the dog's name:

```xml
set myObject.pets[1].name = myObject.pets[0].name
```

Adding Data:

- Add income for Q3 with a value of "$30,000":

```xml
set myObject.income.Q3 = "$30,000"
```

- Add a new car "Tesla" to the array:

```xml
set myObject.cars[] = "Tesla"
```

- Replace the existing value in the array:

```xml
set myObject.cars[0] = "Porsche"
```

Deleting Data:

- Remove income for Q2:

```xml
remove myObject.income.Q2
```

- Delete the second car (BMW):

```xml
remove myObject.cars[1]
```

This is a basic example. Karate's JsonPath expressions allow for more complex manipulations of JSON data structures.