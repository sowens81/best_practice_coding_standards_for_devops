# Python Scripting Standards

## Naming Standards

### Variable Naming

- **Use snake_case** for variable names.
  - Example: `max_retries`, `user_name`
- **Avoid single-letter variable names** unless used in loops or temporary contexts.
- **Use descriptive names** to make the code self-documenting.

### Parameter Naming

- **Use snake_case** for parameter names.
  - Example: `max_retries`, `user_name`
- **Avoid single-letter parameter names**.
- **Use descriptive names** to make the code self-documenting.

### Function and Method Naming

- **Use snake_case** for function and method names.
  - Example: `calculate_total`, `get_user_input`
- **Include a brief description** of the function’s or method’s purpose if it’s not immediately obvious.

### Class Naming

- **Use PascalCase** for class names.
  - Example: `UserManager`, `OrderProcessor`
- **Include a brief description** of the class’s purpose if it’s not immediately obvious.

### File Naming

- **Use snake_case** for filenames.
  - Example: `deploy_script.py`, `cleanup_temp_files.py`
- **Include a descriptive name** and, if applicable, the action or purpose of the script.

### Folder Naming

- **Use snake_case** for folder names.
  - Example: `scripts`, `utils_scripts`

## Coding Standards

### General Guidelines

- **Use consistent indentation** (4 spaces per indentation level, not tabs).
- **Write clear docstrings** for all public modules, functions, classes, and methods.
  - **Use triple double-quoted strings** for docstrings.
  - Example:
  
    ```python
    def calculate_total(amount: float, tax_rate: float) -> float:
        """
        Calculate the total amount after tax.

        Args:
            amount (float): The initial amount.
            tax_rate (float): The tax rate to be applied.

        Returns:
            float: The total amount after tax.
        """
        return amount * (1 + tax_rate)
    ```

- **[https://peps.python.org/pep-0000/](Follow PEP 8)** for style and formatting guidelines.
- **Include error handling** and validation for inputs where appropriate.
- **Use double underscores** for private attributes and methods.
  - Example: `_private_method()`

### Control Structures

- **Use `if` statements** with `and` and `or` for multiple conditions.
  - Example: `if value > 10 and value < 20: ...`
- **Use `elif`** for multiple conditions instead of nested `if` statements.

### Functions and Methods

- **Define functions and methods using snake_case**.
- **Functions and methods should be defined at the top** of your script or in a dedicated module.
- **Include type hints** for function parameters and return types.

## Code Review Standards

### Process

- **Submit pull requests** for code changes.
- **Ensure all changes are reviewed** by at least one other team member before merging.

### Reviewer Responsibilities

- **Check for adherence** to naming and coding standards.
- **Verify code functionality** and error handling.
- **Provide feedback** and suggest improvements where applicable.

### Developer Responsibilities

- **Ensure code is tested** thoroughly before requesting a review.
- **Address feedback** and make necessary revisions in a timely manner.

## Additional Notes

- **Include any additional information** or project-specific guidelines here.
