# LDA Topic Probabilities Calculator

## Description

A web-based tool to calculate topic probabilities for a given word in a document using Latent Dirichlet Allocation (LDA). Users input documents, initial topic assignments, and parameters (alpha, beta) to compute unnormalized and normalized topic probabilities, with results displayed interactively.

## Features

- Input documents and initial topic assignments via text areas.
- Select a target document and word to calculate topic probabilities.
- Adjustable alpha and beta parameters for LDA.
- Displays both unnormalized and normalized probabilities with detailed calculations.
- Built with HTML, Tailwind CSS, JavaScript, and Pyodide (running Python with NumPy in the browser).
- Input validation and error handling for robust user experience.

## Prerequisites

No installation is required as the application runs entirely in the browser using Pyodide. A modern web browser (e.g., Chrome, Firefox, Edge) is sufficient.

## Setup

1. Clone the repository:

   ```bash
   git clone https://github.com/sakibnjr/py_LDA.git
   ```

2. Open index.html in a web browser directly, or serve it using a local server (e.g., with Python):

   ```bash
   python -m http.server 8000
   ```

3. Navigate to http://localhost:8000 in your browser.

## Usage

1. Enter Documents: Input one document per line in the "Documents" textarea, with words separated by spaces (e.g., lion hunts gazelle savanna).

2. Enter Initial Topic Assignments: Input topic assignments for each word in the corresponding document, one per line, with numbers separated by spaces (e.g., 0 0 0 1).

3. Select Target Document and Word: Choose the document index (starting from 0) and a word from the dropdown, which populates based on the selected document.

4. Set Alpha and Beta: Adjust the LDA hyperparameters (default: alpha = 0.1, beta = 0.01).

5. Calculate: Click the "Calculate Probabilities" button to compute and display the topic probabilities.

6. View Results: The results section shows unnormalized probabilities, their sum, and normalized probabilities with percentages.

### Example Input

##### Documents:

```bash
  lion hunts gazelle savanna
  elephants giraffes live africa
  soccer players score goals stadium
```

##### Initial Topic Assignments:

```bash
  0 0 0 1
  0 0 0 1
  1 1 1 1 1
```

##### Target Document Index: 0

##### Target Word: lion

##### Alpha: 0.1

##### Beta: 0.01

### Output:

Displays probabilities for each topic, e.g., P(Topic 0) = 0.1234567 / 0.2345678 ≈ 0.526 (52.6%).

## Acknowledgments

- Built with Pyodide for running Python in the browser.
- Styled with Tailwind CSS.
- Inspired by LDA topic modeling concepts from machine learning literature.
