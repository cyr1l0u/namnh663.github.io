---
layout: default
title: Scripting
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

## GET Request - URL and Path

![](/assets/images/karate/url-path.png)

## Simple Assertions

**Response:**

```json
{
    "tags": [
        "eos",
        "enim",
        "est",
        "ipsum",
        "repellat",
        "quia",
        "exercitationem",
        "tenetur",
        "facilis",
        "consequatur"
    ]
}
```

![](/assets/images/karate/assertions.png)

## POST Request

![](/assets/images/karate/post-request.png)

1. **Login and Get Token:**
    - A username and password are needed to log in.
    - A POST request is made to the `/users/login` endpoint with login credentials in the request body.
    - The response includes an authorization token that will be used in future requests.
2. **Create Article:**
    - The authorization token is obtained from the login response and stored in a variable.
    - A POST request is made to the `/articles` endpoint with the new article data (title and description) in the request body.
    - An authorization header is added to the request with the format: `Authorization: Token <token_value>`.
    - The response is checked for successful creation (status code 200) and the article details are verified.

**Key Points:**

- The authorization token is required for creating new articles.
- The title of the article must be unique to avoid errors.

**Suggestion:**

- Use a random data generator to automatically create unique titles and descriptions for articles in tests.
- Refactor the code to create a separate function for obtaining the authorization token for reusability.

## DELETE Request

![](/assets/images/karate/delete-request.png)