# Task -- Unit Testing and CI Integration

## Purpose of the Task

The purpose of this task was to implement unit tests for a provided Node.js library (https://github.com/petri-rantanen/AT00BY10),
as well to integrate automated testing using GitHub Actions, and generate coverage reports using Coveralls.io

The objectives were:

- Implement unit tests for the library
- Achieve at least 60% code coverage (excluding `.internal`)
- Configure GitHub Actions workflow
- Integrate Coveralls for coverage reporting
- Evaluate the library’s reliability

---

## Installation & Setup

### 1. Initialize project

```bash
git init
npm init -y
```

### 2. Install dependencies

```bash
npm install
```

### 3. Install testing libraries

```bash
npm install --save-dev mocha chai c8
```

---

## Running Tests

```bash
npm test
```

---

## Running Coverage

```bash
npm run coverage
```


---

## Testing Implementation

The following test files were created:

- add.test.js
- at.test.js
- camelCase.test.js
- capitalize.test.js
- castArray.test.js
- get.test.js
- slice.test.js
- words.test.js

Each file tests a specific function of the library.

---

## Coverage Configuration

```json
"c8": {
  "exclude": ["src/.internal/**"]
}
```

---

## Continuous Integration

GitHub Actions pipeline:

- Install dependencies  
- Run tests  
- Generate coverage  
- Upload to Coveralls  

---

## Coverage Report

[![Coverage Status](https://coveralls.io/repos/github/lehacamry/FinalTask/badge.svg?branch=main)](https://coveralls.io/github/lehacamry/FinalTask?branch=main)

---

## Project Structure

```
.
├── .github/workflows/
├── src/
├── test/
├── package.json
├── README.md
├── LICENSE
├── .gitignore
```

---

## Issues

No critical issues were identified during testing. When i pushed files from local mashine to gitHub for first time, my ./internal folder for some reason missed, and GitHub Action test wasn't successful. Repushing of files helped 

---

## Summary

This project demonstrates unit testing, CI integration, and coverage reporting.

---

## License

This project is licensed under the MIT License.  
See the LICENSE file for details.

