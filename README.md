# Calculator-CLI-with-Typescript

A simple command-line calculator built with Node.js and TypeScript. It performs basic arithmetic operations such as addition, subtraction, multiplication, and division directly from the terminal.

## Features

- **Command-Line Interface:** Interactive input using `readline-sync`
- **Basic Operations:** Supports `+`, `-`, `*`, `/`
- **Input Validation:** Ensures only valid numbers and operators are accepted
- **Recursive Retry:** Prompts user again on invalid input
- **Lightweight & Fast:** No external dependencies except for input handling

## Technologies Used

- **Runtime:** Node.js
- **Language:** TypeScript (compiled to JavaScript)
- **Package:** readline-sync for CLI input handling

## Prerequisites

Before running this application, make sure you have the following installed:

- Node.js (v14 or higher)
- npm (Node Package Manager)
- TypeScript (optional, for editing or recompiling the `.ts` file)

## Installation

1. Clone the repository:
    ```bash
    git clone <repository-url>
    cd calculator-cli
    ```
2. Install dependencies:
    ```bash
    npm install
    ```
3. (Optional) If you wish to modify and recompile the TypeScript file:
    ```bash
    tsc index.ts
    ```

## Usage

1. Run the application:
    ```bash
    node index.js
    ```
2. Enter the first number when prompted
3. Enter an operator (`+`, `-`, `*`, `/`)
4. Enter the second number
5. The result will be displayed instantly

Example:

```yaml
Enter first number: 10
Enter operator: *
Enter second number: 5
Result: 50
```

If invalid input is provided, the program displays an error message and prompts again.

## File Structure

```bash
calculator-CLI/
├── .git/           # Git version control directory
├── .gitignore      # Git ignore file
├── index.js        # Compiled JavaScript file
├── index.ts        # TypeScript source file
├── package-lock.json # Auto-generated lock file for npm
├── package.json    # Project metadata and dependencies
└── README.md       # This documentation file
```

## How It Works

1. The program uses readline-sync to capture user input from the terminal
2. Input values are validated to ensure both operands are numbers and operator is valid
3. The calculation is performed based on the selected operator
4. The result is displayed to the user in the console

## Configuration

To modify or extend functionality:
- Update `calculate()` function in `index.ts` to add new operations
- Adjust input prompts in `main()` for custom UI messages

## Known Issues

1. **Integer Parsing Only:** Currently supports integer inputs (parseInt)
2. **Division by Zero:** No explicit handling yet for zero-division
3. **No Floating Point Support:** Results are rounded to integer values

## Troubleshooting

### Command Not Found

- Ensure Node.js and npm are correctly installed
- Use node -v and npm -v to verify installation

### Invalid Input Repeats

- Enter valid numerical values and one of the four supported operators

### Security Considerations

- Runs locally in the terminal — no external network or file operations
- Safe for use in educational and offline environments

### Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request