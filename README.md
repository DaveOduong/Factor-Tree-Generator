# Factor Tree Generator

## Overview

Factor Tree Generator is a simple web-based educational tool that visually breaks down a number into its prime factors using a factor tree. The application automatically generates an interactive SVG diagram and displays the prime factorization in exponential form.

This project is built entirely with HTML, CSS, and JavaScript and runs directly in a web browser without requiring any external libraries.

---

## Features

* Generate factor trees for numbers from 2 to 99,999
* Automatic prime factor detection
* Visual SVG-based factor tree rendering
* Color-coded nodes:

  * Green = Prime numbers
  * Red = Composite numbers
* Displays prime factorization using exponent notation
* Input validation and error handling
* Responsive horizontal scrolling for large trees
* No external dependencies

---

## Technologies Used

* HTML5
* CSS3
* Vanilla JavaScript
* SVG Graphics

---

## How It Works

### Step 1: Input

Enter a positive integer between 2 and 99,999.

### Step 2: Factorization

The program repeatedly finds the smallest factor of the number and recursively splits it until only prime numbers remain.

Example:

90

↓

2 × 45

↓

2 × (3 × 15)

↓

2 × (3 × (3 × 5))

### Step 3: Visualization

The factor tree is drawn using SVG elements:

* Circles represent numbers
* Lines connect parent and child factors
* Prime nodes are colored green
* Composite nodes are colored red

### Step 4: Prime Factor Form

The final factorization is displayed in exponential notation:

90 = 2 × 3² × 5

---

## Project Structure

```text
Factor Tree Generator
│
├── index.html
│
├── HTML
│   ├── Input field
│   ├── Generate button
│   ├── Tree display area
│   └── Result section
│
├── CSS
│   ├── Layout styling
│   ├── Node colors
│   └── Responsive design
│
└── JavaScript
    ├── smallestFactor()
    ├── isPrime()
    ├── buildTree()
    ├── indexLeaves()
    ├── calcXY()
    ├── treeDepth()
    ├── renderSVG()
    ├── factorMap()
    └── generate()
```

---

## Algorithms Used

### Prime Testing

Determines whether a number is prime by finding its smallest factor.

Time Complexity:
O(√n)

### Recursive Factor Tree Construction

Builds a binary tree where each composite number is split into two factors until all leaves are prime.

### Tree Layout Algorithm

Calculates node positions using leaf indexing and depth-based spacing to ensure a clean visual structure.

### Prime Factorization

Counts occurrences of each prime factor and displays them using exponent notation.

Example:

```text
360 = 2³ × 3² × 5
```

---

## Example Output

Input:

```text
90
```

Factor Tree:

```text
        90
       /  \
      2   45
         /  \
        3   15
           / \
          3   5
```

Prime Factorization:

```text
90 = 2 × 3² × 5
```

---

## Validation Rules

* Input must be an integer
* Minimum value: 2
* Maximum value: 99,999
* Invalid inputs generate user-friendly error messages

---

## Educational Applications

This tool can be used for:

* Learning prime factorization
* Understanding factor trees
* Teaching number theory concepts
* Mathematics classroom demonstrations
* Self-study and revision

---

## Future Enhancements

* Dark mode
* Tree animation effects
* Export tree as PNG
* Export tree as PDF
* Display all factors of a number
* Greatest Common Divisor (GCD) calculator
* Least Common Multiple (LCM) calculator
* Multiple-number factor tree comparison
* Mobile app version

---

## Author

Developed as a lightweight educational mathematics visualization tool using HTML, CSS, JavaScript, and SVG graphics.

---

## License

This project is free to use for educational and personal purposes.
