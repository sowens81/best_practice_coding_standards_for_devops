# Terraform Standards

## Naming Standards

### Variable Naming

- **Use snake_case** for variable names.
  - Example: `instance_type`, `region`
- **Avoid single-letter variable names** unless used in loops or temporary contexts.
- **Use descriptive names** to make the code self-documenting.

### Resource Naming

- **Use snake_case** for resource names.
  - Example: `aws_instance_web_server`, `google_storage_bucket_logs`
- **Include a brief description** of the resource’s purpose if it’s not immediately obvious.

### Module Naming

- **Use snake_case** for module names.
  - Example: `networking_module`, `compute_instance_module`
- **Include a brief description** of the module’s purpose if it’s not immediately obvious.

### File Naming

- **Use snake_case** for filenames.
  - Example: `main.tf`, `variables.tf`, `outputs.tf`, `version.tf`, `provider.tf`
- **Include a descriptive name** and, if applicable, the action or purpose of the file.

### Folder Naming

- **Use snake_case** for folder names.
  - Example: `modules`, `environments`

## Folder Structure for a Terraform Project

A typical Terraform project or module might have the following folder structure:

### `modules/` Folder

- **Contains reusable modules** Modules will not container a provider instance.
- Each module directory follows the file structure:
  - `main.tf`: Contains the main configuration for the module.
  - `variables.tf`: Defines the module’s variables.
  - `outputs.tf`: Defines the outputs of the module.
  - `version.tf`: Specifies the Terraform version and provider versions.
  - `README.md`: Contains information about the module and how to use it.

### Root Level Files

- `main.tf`: Contains root-level configurations and possibly includes module references.
- `variables.tf`: Defines root-level variables if not fully defined within modules.
- `outputs.tf`: Defines root-level outputs if not fully defined within modules.
- `version.tf`: Specifies the Terraform version and provider versions for the whole project.
- `provider.tf`: Configures providers for the whole project.

## Coding Standards

### General Guidelines

- **Follow the [HashiCorp Configuration Language (HCL)](https://www.terraform.io/docs/configuration/syntax.html) style guide** for formatting and style.
- **Use consistent indentation** (2 spaces).
- **Write clear comments** explaining the purpose of resources, modules, and variables.
- **Organize Terraform code** into modules to promote reusability and maintainability.
- **Use Terraform's built-in validation** and linting tools to check for errors and style issues.
- **Include `terraform fmt`** to format Terraform code according to the canonical style.
- **Use `terraform validate`** to validate the configuration files.

### Variables and Outputs

- **Define variables using `variable` blocks** and provide descriptions for clarity.
  - Example:
  
    ```hcl
    variable "instance_type" {
      description = "Type of the instance to create."
      type        = string
      default     = "t2.micro"
    }
    ```

- **Define outputs using `output` blocks** to expose values from modules or configurations.
  - Example:
  
    ```hcl
    output "instance_id" {
      description = "The ID of the created instance."
      value       = aws_instance.web_server.id
    }
    ```

### Resource Blocks

- **Use clear and descriptive names** for resources.
- **Include tags** for resource identification and management, where applicable.

## Code Review Standards

### Process

- **Submit pull requests** for code changes.
- **Ensure all changes are reviewed** by at least one other team member before merging.

### Reviewer Responsibilities

- **Check for adherence** to naming and coding standards.
- **Verify resource configurations** and ensure they meet the intended requirements.
- **Provide feedback** and suggest improvements where applicable.

### Developer Responsibilities

- **Ensure Terraform configurations are tested** thoroughly before requesting a review.
- **Address feedback** and make necessary revisions in a timely manner.

## Additional Notes

- **Include any additional information** or project-specific guidelines here.
