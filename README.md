# Code Overview
URL of project used: https://github.com/Ayon-SSP/Calcky.git
The code is intended to perform basic arithmetic operations (`+`, `-`, `*`, `/`) and exponentiation (`^`). It reads two numbers and an operator from the user, performs the specified operation, and prints the result.

# Detailed Analysis

## 1. Variable Declarations

- `float n1, n2, n3;`:
  - `n1` and `n2` are used for the numbers involved in the operation.
  - `n3` is declared but not used in the current implementation.

- `float div, pro;`:
  - `div` is used to store the result of division.
  - `pro` is used to store the result of exponentiation.

- `char signe, signe2;`:
  - `signe` stores the operator for the operation.
  - `signe2` is declared but not used.

## 2. Reading Input

- `cin >> n1;` reads the first number.
- `cin >> signe;` reads the operator.
- `cin >> n2;` reads the second number.
- `signe2` and `n3` are commented out and not used in the current version of the code.

## 3. Exponentiation Calculation

- `pro = 1;` initializes `pro` to 1.
- `for (int i = 1; n2 >= i; i++) { pro = pro * n1; }`:
  - This loop computes `n1` raised to the power of `n2`. It multiplies `n1` by itself `n2` times.
  - Note: This implementation only works for non-negative integer values of `n2`.

## 4. Switch-Case for Operations

- **Addition (`+`)**: `cout << n1 + n2;` adds `n1` and `n2` and prints the result.
- **Subtraction (`-`)**: `cout << n1 - n2;` subtracts `n2` from `n1` and prints the result.
- **Division (`/`)**: `div = n1 / n2;` divides `n1` by `n2` and prints the result. No handling of division by zero is implemented.
- **Multiplication (`*`)**: `cout << n1 * n2;` multiplies `n1` and `n2` and prints the result.
- **Exponentiation (`^`)**: `cout << pro;` prints the result of `n1` raised to the power of `n2`.
- **Default Case**: `cout << "nothing";` handles invalid operators by printing "nothing".

# Improvements and Considerations

## 1. Handling Division by Zero

- Add a check to ensure `n2` is not zero before performing division to avoid runtime errors.

## 2. Handling Non-integer Exponentiation

- The current implementation only handles positive integer exponents. For non-integer or negative exponents, a more complex algorithm or library function would be required.

## 3. Unused Variables

- Remove or utilize `signe2` and `n3` if they were intended for additional functionality.

## 4. Input Validation

- Validate user input to handle cases where input might not be a valid number or operator.

## 5. Code Structure

- Refactor the exponentiation logic into a separate function to improve readability and maintainability.
