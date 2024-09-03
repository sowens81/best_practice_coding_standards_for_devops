# PowerShell Scripting Standards

## Naming Standards

### Variable Naming

- **Use camelCase** for variable names.
  - Example: `maxRetries`, `userName`
- **Avoid single-letter variable names** unless used in loops or temporary contexts.
- **Use descriptive names** to make the script self-documenting.

### Parameter Naming

- **Use PascalCase** for parameter names.
  - Example: `MaxRetries`, `UserName`
- **Avoid single-letter parameter names**.
- **Use descriptive names** to make the script self-documenting.

### Function and Class

- **Use PascalCase** for function names, classes, and models.
  - Example: `CalculateTotal`, `GetUserInput`, `UserModel`
- **Include a brief description** of the function’s or class’s purpose if it’s not immediately obvious.

### File Naming

- **Use snake_case** for script filenames.
  - Example: `deploy_script.ps1`, `cleanup_temp_files.ps1`
- **Include a descriptive name** and, if applicable, the action or purpose of the script.

### Folder Naming

- **Use snake_case** for folder names.
  - Example: `scripts`, `utils_scripts`

## Coding Standards

### General Guidelines

- **Use `#requires -Version`** at the top of your script to specify the required PowerShell version if applicable.
- **Use consistent indentation** (2 or 4 spaces, not tabs).
- **Write clear comments** explaining the purpose of sections and complex logic.
- **Include error handling** and validation for inputs.
- **Use double quotes** around variable references to avoid issues with interpolation and escaping.
  - Example: `Write-Output "$variable"`

### Control Structures

- **Use `if` statements** with `-and` and `-or` for multiple conditions.
  - Example: `if ($value -gt 10 -and $value -lt 20) { ... }`
- **Use `switch` statements** for multi-condition checks instead of multiple `if` statements where appropriate.

### Functions, Classes, and Models

- **Define functions, classes, and models using PascalCase**.
- **Functions**: Define functions at the top of your script or in a dedicated module.
- **Classes and Models**: If applicable, use PascalCase for class and model definitions.
  - Example: `UserManager`, `OrderProcessor`

## Code Review Standards

### Process

- **Submit pull requests** or merge requests for code changes.
- **Ensure all changes are reviewed** by at least one other team member before merging.

### Reviewer Responsibilities

- **Check for adherence** to naming and coding standards.
- **Verify script functionality** and error handling.
- **Provide feedback** and suggest improvements where applicable.

### Developer Responsibilities

- **Ensure scripts are tested** thoroughly before requesting a review.
- **Address feedback** and make necessary revisions in a timely manner.

## Additional Notes

- **Include any additional information** or project-specific guidelines here.
