# BIC21203 Web Development — Lab #4b: Client-Side Scripting (JSON and jQuery)

**Institution:** Universiti Tun Hussein Onn Malaysia (UTHM)  
**Faculty:** Faculty of Computer Science and Information Technology (FSKTM)  
**Course:** BIC21203 Web Development  

---

## Overview

This repository contains the client-side scripting exercises for **Lab #4b**, demonstrating how to:
1. Structure valid **JSON** datasets with nested objects and arrays (`books.json`).
2. Asynchronously retrieve, parse, and safely render JSON data into the DOM using the native JavaScript **`fetch()` API** (`books.html`).
3. Perform equivalent DOM updates and event handling using **jQuery 4.0.0** (`.text()`, `.addClass()`, and `.on()`) compared to vanilla JavaScript (`jquery-dom.html`).

---

## Expected Outputs & Screenshots

### Question 1: Valid JSON Dataset (`books.json`)
- Contains a top-level `"books"` array with two book objects, double-quoted property names, numeric `publicationYear`, and string-array `genres`.
- Verified using `JSON.parse()` in the browser Developer Tools Console (`F12`).

[books.json Code] 
<img width="358" height="279" alt="image" src="https://github.com/user-attachments/assets/3eed413b-6c73-4a64-b094-5af06bcb7900" />


[JSON.parse() Confirmation] 
<img width="164" height="25" alt="image" src="https://github.com/user-attachments/assets/438efc98-2ac4-4ccf-bf8d-b07f7a157fc3" />


### Question 2: Fetch & Display JSON (`books.html`)
- Retrieves `books.json` asynchronously over HTTP and safely inserts text using `createElement()` and `textContent`.
- Displays:
  - **First Book Title:** The Great Gatsby
  - **Second Book Author:** Harper Lee
  - **Genres Grouped by Book:**
    - The Great Gatsby: Fiction, Classics
    - To Kill a Mockingbird: Fiction, Coming-of-Age

[books.html Browser Output] 
<img width="449" height="237" alt="image" src="https://github.com/user-attachments/assets/0b1c953f-35d3-4b29-bfa8-81a71ad56894" />


### Question 3: jQuery DOM & Event Comparison (`jquery-dom.html`)
- Uses jQuery 4.0.0 (`https://code.jquery.com/jquery-4.0.0.min.js`) to:
  1. Replace `#myElement` text with `"Modified Text"` via `.text()`.
  2. Apply the `.myStyle` CSS class (`background-color: coral; padding: 16px;`) to `#myDIV` via `.addClass()`.
  3. Trigger an `alert("Button clicked!")` dialog on `#myButton` click via `.on("click", ...)`.

[jquery-dom.html Output and Alert] 
<img width="1273" height="258" alt="image" src="https://github.com/user-attachments/assets/48ec216c-7ec6-4179-a7ca-a8166e0ac8ef" />
