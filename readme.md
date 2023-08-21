---

# Search Page XSS Example

## Overview

This project is a simple, educational demonstration of a Cross-Site Scripting (XSS) vulnerability, specifically designed to show how a web application might be susceptible to this type of attack. This example was made for a demo during a presentation on cyber security at my school.

### Technologies Used

- HTML
- JavaScript
- Tailwind CSS

## How it Works

The code consists of a basic search page with an input field and a search button. When the user inputs text into the search bar and clicks the "Search" button, the query is directly injected into the page's HTML without proper sanitization. This lack of sanitization is what leads to the XSS vulnerability.

A common defense against XSS is built into modern browsers, which prevents most direct attacks using `innerHTML`. However, this example provides a specific way to bypass this protection, using an `<img>` tag with an `onerror` attribute.

### Example Exploit

A user can enter the following code into the search bar and execute the search:

```html
<img src='x' onerror='alert("You have been hacked!")'>
```

This will trigger a JavaScript alert, showcasing the vulnerability.

## Why This is Important

Cross-Site Scripting is one of the most common security vulnerabilities on the web. This project serves as a simple demonstration to raise awareness of this issue and to educate developers on the importance of properly sanitizing user input.

## How to Run

Open the HTML file :)

## Disclaimer

This project is meant for educational purposes only. Please do not use this code in production environments, as it intentionally contains security flaws.

---
