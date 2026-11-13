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

## Repository Structure

```text
├── books.json          # Question 1: Valid JSON dataset containing book metadata and genre arrays
├── books.html          # Question 2: Fetches books.json via HTTP and renders selected fields safely
├── jquery-dom.html     # Question 3: Demonstrates jQuery 4.0.0 DOM manipulation and click event handling
├── screenshots/        # Folder containing output screenshots for documentation
└── README.md           # Setup instructions, project overview, and output evidence
```

---

## Setup & Execution Instructions

> **Important Note:** Do **not** open `books.html` directly via the `file://` protocol. Modern browsers block `fetch()` requests to local files due to CORS security policies. Use a local HTTP development server instead.

### Running with VS Code Live Server
1. **Clone or download this repository:**
   ```bash
   git clone <your-github-repository-url>
   cd <repository-folder-name>
   ```
2. **Open the folder in Visual Studio Code:**
   - Go to `File > Open Folder...` and select the project directory.
3. **Install the Live Server extension (if not already installed):**
   - Open Extensions (`Ctrl + Shift + X`), search for **Live Server** by *Ritwick Dey*, and click **Install**.
4. **Launch the web pages:**
   - Right-click `books.html` in the VS Code Explorer and select **Open with Live Server**.
   - Your browser will open at `http://127.0.0.1:5500/books.html`.
   - Open `http://127.0.0.1:5500/jquery-dom.html` to view Question 3.

---

## Expected Outputs & Screenshots

*(Save your screenshots inside a `screenshots/` folder in your repository and ensure the filenames match the paths below.)*

### Question 1: Valid JSON Dataset (`books.json`)
- Contains a top-level `"books"` array with two book objects, double-quoted property names, numeric `publicationYear`, and string-array `genres`.
- Verified using `JSON.parse()` in the browser Developer Tools Console (`F12`).

![books.json Code](screenshots/q1-books-json.png)
![JSON.parse() Confirmation](screenshots/q1-json-parse.png)

### Question 2: Fetch & Display JSON (`books.html`)
- Retrieves `books.json` asynchronously over HTTP and safely inserts text using `createElement()` and `textContent`.
- Displays:
  - **First Book Title:** The Great Gatsby
  - **Second Book Author:** Harper Lee
  - **Genres Grouped by Book:**
    - The Great Gatsby: Fiction, Classics
    - To Kill a Mockingbird: Fiction, Coming-of-Age

![books.html Browser Output](screenshots/q2-books-html.png)

### Question 3: jQuery DOM & Event Comparison (`jquery-dom.html`)
- Uses jQuery 4.0.0 (`https://code.jquery.com/jquery-4.0.0.min.js`) to:
  1. Replace `#myElement` text with `"Modified Text"` via `.text()`.
  2. Apply the `.myStyle` CSS class (`background-color: coral; padding: 16px;`) to `#myDIV` via `.addClass()`.
  3. Trigger an `alert("Button clicked!")` dialog on `#myButton` click via `.on("click", ...)`.

![jquery-dom.html Output and Alert](screenshots/q3-jquery-dom.png)